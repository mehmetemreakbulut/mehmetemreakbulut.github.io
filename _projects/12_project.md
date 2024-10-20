---
layout: page
title: Apache Spark Educational
description: Educational Apache Spark Project
img: assets/img/apache-spark.png
importance: 1
category: fun
related_publications: false
---

<a href="https://github.com/mehmetemreakbulut/apache-spark-educational">Github Page</a>
<br><br>

### Educational Apache Spark Project

This Java code is part of an educational project using Apache Spark to process and analyze educational data. The code is structured to read data from CSV files, perform transformations, and execute both batch and streaming queries. Here's a detailed explanation of the code:

1. **Package and Imports**: The code begins by declaring the package and importing necessary classes from the Apache Spark library. These imports include classes for Spark SQL, streaming, and data types.

2. **Class Declaration**: The main class `SparkGroup38` is declared, which contains the main method and other necessary components.

3. **Constants**: A constant `numCourses` is defined, which is used later in the streaming query.

4. **Main Method**: The `main` method is the entry point of the application. It accepts command-line arguments for the Spark master URL and the file path.

5. **Spark Session Initialization**: A Spark session is created with the specified master URL and application name. The log level is set to "ERROR" to reduce verbosity.

6. **Schema Definition**: Schemas for three datasets (`profs`, `courses`, and `videos`) are defined using `StructType` and `StructField`. These schemas specify the structure of the CSV files to be read.

7. **Reading CSV Files**: The code reads three CSV files (`profs.csv`, `courses.csv`, and `videos.csv`) into Spark DataFrames using the defined schemas. The `option` method is used to specify that the CSV files do not have headers and use commas as delimiters.

8. **Reading Streaming Data**: A streaming DataFrame `visualizations` is created using the `rate` source, which generates rows at a specified rate (`rowsPerSecond`). The `value` column is used to simulate video IDs.

9. **Data Transformation and Caching**:
   - `videosWithCourse`: This DataFrame is created by joining the `videos` and `courses` DataFrames on the `course_name` column. It is cached to avoid recomputation in subsequent queries.
   - `profWithCourse`: This DataFrame is created by joining the `profs` and `courses` DataFrames on the `course_name` column. It is used only once, so it is not cached.

10. **Query Q1**: This query computes the total number of lecture hours per professor. It groups the `profWithCourse` DataFrame by `prof_name` and sums the `course_hours`. The result is displayed using the `show` method.

11. **Query Q2**: This streaming query computes the total duration of all visualizations of videos for each course over a minute, updated every 10 seconds. It joins the `visualizations` DataFrame with `videosWithCourse`, groups by a time window and `course_name`, and sums the `video_duration`. The result is written to the console in "update" mode.

12. **Query Q3**: This streaming query computes the total number of visualizations of each video with respect to the number of students in the course. It joins the `visualizations` DataFrame with `videosWithCourse`, groups by `video_id` and `course_students`, counts the visualizations, and computes the ratio of visualizations to students. The result is written to the console in "update" mode.

13. **Await Termination**: The code waits for the streaming queries (`q2` and `q3`) to terminate. If an exception occurs, it is caught and printed.

14. **Spark Session Close**: Finally, the Spark session is closed to release resources.

Overall, this code demonstrates how to use Apache Spark for both batch and streaming data processing in an educational context, providing insights into lecture hours, video visualizations, and student engagement.
