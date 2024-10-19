---
layout: page
title: SONAR
description: A Helpful Tool for Academia, Awarded by Bogazici University Computer Engineering Department
img: assets/img/sonar/sonar-ui3.png
importance: 1
category: graphs
related_publications: false
---
<a href="https://github.com/yusuferdemnacar/sonar-backend">Github Page</a>
<br><br>
◦ Analysis of the scholarly network using graph theory and relevant metrics <br>
◦ A tool with Graph UI for researchers to explore scholarly network in an efficient way for article recommendations,
finding research groups, literature review, etc
<br>

Today, many articles are published by many organizations and researchers. It has
become very difficult to follow up-to-date research published in a certain academic field.
In addition to all these, when we also consider the interrelationship of academic studies
in different fields, we see a wide network. In our project, Social Network Analysis on
Research, we aim to create a publicly available web application/tool that showcases
these relationships and uses them in a specific domain. In this way, we think that
everyone, from undergraduate students to university professors, will have the chance
to examine and analyze academic knowledge in a particular field.
Seeing which academic writers have participated in such studies, examining the connections between citations, and seeing the clusters formed are supportive of academic studies.

Identifying rapidly developing sub-disciplines, seeing influential authors in a particular academic field, or analyzing the reflection of a current issue in academia are
some of the possible outcomes within the academic environment. One of these current
issues is naturally COVID-19. A time-dependent graph and analysis can be created
on COVID-19 using the tool. In the last few years, the publicly presented COVID-19
graph can explain which articles, authors, organizations, or journals in academia have
been effective on this subject, in conjunction with their relations with each other.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sonar/sonar-ui.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sonar/sonar-ui2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sonar/sonar-ui4.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
We have revised the design and implementation of the SONAR application. The
application now provides a complete API that performs the tasks described in the
previous sections.
We have implemented a user interface that provides users with an easier way to
access the functionalities of the API.
We have investigated the possible connections that can be constructed between
other graph-structured knowledge representations and our research graphs and created
interfaced graphs for proof of concepts
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/sonar/sonar-ui2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
</div>
Social Network Analysis is a method used to derive meaningful information on
many datasets showing graph structure. In this direction, we conducted a literature
survey to understand how it is used in different fields. ”Social Network Analysis:
Methods and Applications” [2] has been very influential in shaping our basic ideas
about Social Network Analysis. ”Models and Methods in Social Network” [1], which is
also its sequel helped us to understand what skill sets we need to progress within our
project.
We continued to direct our research in line with cluster analysis and graph theory.
Especially, we have focused on the meaning of graph metrics in our research graph.
Additionally, we have benefited from works such as ”On the Correlation between
Research Performance and Social Network Analysis Measures Applied to Research
Collaboration Networks” [6] and ”Polarized public opinion responding to corporate
social advocacy: Social network analysis of boycotters and advocators” [5] helped us
get better insight into the meaning and usage of our metrics as well as helped us think
about questions that we may want to do research on.
Additionally, works on the topological structure of social networks such as ”Graph
pattern matching revised for social network analysis” [3] helped us understand the
technical methodology used in doing research on social network analysis.
As a result, we have observed that social network analysis is a method that is
widely used in different domains, however, analyzing authorship and citation graph in
terms of their domains can help to uncover the dynamics of research graphs and also
academia.

The Django server is deployed in an EC2 instance using Amazon Web services. Also,
the Postgresql server is deployed in another EC2 Server. Digital Ocean Droplet is used
for Graph Database Neo4j Server. The Django server is communicating with both of
the database servers.

#### REFERENCES

[1] L. Rossoni, “Models and methods in social network analysis,” 2006.

[2] S. Wasserman and K. Faust, “Social Network Analysis: Methods and Appli-
cations,” 1994.

[3] W. Fan, “Graph pattern matching revised for social network analysis,” 2012.

[4] K. Lo, L. L. Wang, M. Neumann, R. M. Kinney, and D. S. Weld, “S2ORC:
The Semantic Scholar Open Research Corpus,” 2020.

[5] H. Rim, Y. Lee, and S. Yoo, “Polarized public opinion responding to corpo-
rate social advocacy: Social network analysis of boycotters and advocators,” Public
Relations Review, vol. 46, p. 101869, 2020.

[6] A. Abbasi and J. Altmann, “On the Correlation between Research Perfor-
mance and Social Network Analysis Measures Applied to Research Collaboration Net-
works,” 2011 44th Hawaii International Conference on System Sciences, pp. 1–10,
2011.

[7] Z. Kraljevic et al., “Multi-domain Clinical Natural Language Processing with
MedCAT: the Medical Concept Annotation Toolkit,” Artificial intelligence in medicine,
vol. 117, p. 102083, 2020.

[8] O. Bodenreider, “The Unified Medical Language System (UMLS): integrating
biomedical terminology,” Nucleic acids research, vol. 32 Database issue, pp. D267-70,
2004.
