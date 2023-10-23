---
title: "Research | Wang Research Group | Department of Mathematics and Computer Science at Tougaloo College"
layout: gridlay
excerpt: "Research | Wang Research Group | Department of Mathematics and Computer Science at Tougaloo College"
sitemap: false
permalink: /research/
---

# Research

Our overarching goal is to utilize high-throughput genomic and transcriptome data sets, predominantly based on Nanopore long-read sequencing, to investigate the role of DNA methylation in shaping RNA velocity trajectories across diverse biological systems and diseases. We hypothesize that DNA methylation influences gene expression regulation and reshapes RNA velocity trajectories. To address this hypothesis, we will develop innovative computational tools and leverage Nanopore long-read sequencing technology. These tools will enable us to accurately estimate RNA velocity and detect DNA methylation patterns, including rare or novel modifications.

Here are some themes and techniques that we currently work on:

<!-- ![]({{ site.url }}{{ site.baseurl }}/images/respic/venn_diagram.jpg){: style="width: 300px; float: right; border: 10px"} -->

<!-- **RNA Velocity Estimation**  
We will develop a computational toolbox that accurately estimates RNA velocity from Nanopore long-read RNA sequencing data. Leveraging the unique advantages of long-read sequencing, including rich signal-level information, our toolbox will model cell state dynamics based on RNA velocity, spliced/unspliced RNA abundances, latent times, and transcriptional states. The performance of our tool will be rigorously validated by comparing it to existing methods.

**Transformer-Based Detection of DNA Methylation in Nanopore Sequencing**  
We will develop a transformer-based machine learning tool for the direct detection of DNA methylation and evaluate its performance in diverse biological systems and diseases. Leveraging the signal-level information provided by Nanopore long-read sequencing, our novel transformer architecture will accurately detect DNA methylation patterns, including rare or novel modifications like 5hmC. The performance of our approach will be compared to existing methods for detecting DNA methylation using independent datasets.

**RNA Velocity and DNA Methylation: Integrated Analysis**  
We will investigate the relationship between RNA velocity trajectories and DNA methylation patterns across diverse biological systems and diseases. Our computational tools will integrate RNA velocity and DNA methylation data to explore the interplay between these two regulatory mechanisms across different cell types and disease conditions. -->

{% assign number_printed = 0 %}
{% for project in site.data.projects %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if project.highlight == 1 %}

{% if even_odd == 0 %}
<div class="row">
{% endif %}

<div class="col-sm-6 clearfix">
 <div class="well">
  <pubtit>{{ project.title }}</pubtit>
  <img src="{{ site.url }}{{ site.baseurl }}/images/respic/{{ project.image }}" class="img-responsive" width="33%" style="float: left" />
  <p>{{ project.description }}</p>
  <!-- <p><em>{{ project.authors }}</em></p> -->
  <p><strong><a href="{{ project.link.url }}">{{ project.link.display }}</a></strong></p>
  <p class="text-danger"><strong> {{ project.news1 }}</strong></p>
  <p> {{ project.news2 }}</p>
 </div>
</div>

{% assign number_printed = number_printed | plus: 1 %}

{% if even_odd == 1 %}
</div>
{% endif %}

{% endif %}
{% endfor %}

{% assign even_odd = number_printed | modulo: 2 %}
{% if even_odd == 1 %}
</div>
{% endif %}

<p> &nbsp; </p>