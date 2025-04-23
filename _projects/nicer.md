---
layout: page
title: NICER Pulsar Analysis
description: Going beyond radio
img: assets/img/projects/nicer.png
importance: 2
category: "Pulsar astronomy"
---

Understanding the noise in pulsar timing arrays (PTAs) is an ever-growing research field.
One of the best ways to understand frequency-dependent effects caused by the interstellar medium is to use high-energy photons, which are effectively impervious to path-dependent propagation effects as they travel to Earth.
We can use X-ray data obtained by NICER to explore the possibility of mis-modeled chromatic noise across the MSP population.
We can get the associated amplitude and spectral index values for the red noise (RN) using analysis techniques similar to radio data.
Since X-ray data can be (effectively) evenly sampled across time, we can also measure the Modified Allan Variance, a standard for atomic clock errors, by sampling different red noise and white noise combinations from the traditional techniques and creating different realizations of the NICER residuals.
We determine the variance for each pulsar in our array, which we can then use to compare the red noise spectral index and gamma results found with those of the traditional techniques.
We then compare these results to radio data to discuss any chromatic effects evident in the analysis.

<div class="row justify-content-sm-center">
    <div class="col-sm-6 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/projects/nicer.png" title="NICER instrument diagram" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
   The NICER instrument. 
</div>
