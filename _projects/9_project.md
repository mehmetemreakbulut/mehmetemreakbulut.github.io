---
layout: page
title: Multivariate Time Series Analysis with Deep Learning Solutions
description:
img: assets/img/time-series/seasonality.jpeg
importance: 1
category: ml
related_publications: false
---

<a href="https://github.com/mehmetemreakbulut/multivariate-time-series-analysis-dlsolutions">Github Page</a>
<br><br>
[PDF](https://github.com/mehmetemreakbulut/multivariate-time-series-analysis-dlsolutions/blob/master/report.pdf)

In the end, our best performing submission was BiLSTM with Convolutional Layer with an MSE score of 0.010 in the final phase of the
competition. Even though the transformer,that is built from scratch, is a larger model,
it didn’t manage to surpass the BiLSTM, getting a score of 0.011 in the final phase.

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/time-series/bilstmmodel.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>

    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/time-series/pos-encoding.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <p>BiLSTM Model  --  Positional Encoding</p>
</div>

  <div class="row">
      <div class="col-sm mt-3 mt-md-0">
          {% include figure.liquid loading="eager" path="assets/img/time-series/seasonality.jpeg" title="example image" class="img-fluid rounded z-depth-1" %}
      </div>

      <div class="col-sm mt-3 mt-md-0">
          {% include figure.liquid loading="eager" path="assets/img/time-series/similarity.png" title="example image" class="img-fluid rounded z-depth-1" %}
      </div>
  </div>
  <div class="caption">
      <p>Seasonality  --  Similarity</p>
      </div>
