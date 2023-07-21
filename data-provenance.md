---
layout: default
title: Data Provenance
nav_order: 4
---

# Data Provenance

Anyone who has worked with archival materials before (which we may assume encompasses some of the lesson's intended audience!) is likely familiar with the concept of provenance, referring to the origins of something (e.g. a collection or archival fonds). Data provenance, then, traces the origins and lineage of your dataset throughout its lifecycle including:
* where you got the data from
* what transformations your performed upon the data
* what steps you took during your analysis of the data and the thinking behind it

Documenting the provenance of your data helps to establish the accuracy, reliability and [authenticity of your results](https://ardc.edu.au/resource/data-provenance/) and also allows you to trace back and correct errors when you discover them later in the textual data analysis workflow. It is also good practice to make well-named (i.e. easy to identify from the filename alone) copies of the dataset as you move through the stages of the workflow to avoid unintentionally and irreversibly transforming the data.

If you are using a tool like OpenRefine for pre-processing, some of the provenance documentation can be automated; as we will see in "[Exporting the Data](lessons/3-output.html)," OpenRefine keeps track of every operation you perform which can be exported in JSON format.

A more detailed discussion of data provenance is outside of the scope of the current lesson, but if you wish to pursue the topic further, "[Datasheets for Datasets](https://arxiv.org/abs/1803.09010)" by Gebru et al. offers a thorough introduction - and a thoughtful approach - to the topic. For other provenance tools, you can explore Paolo Missier's "[Provenance Standards](http://homepages.cs.ncl.ac.uk/paolo.missier/doc/Provenance-standards.pdf)" and the [Provenance Tools page](https://projects.iq.harvard.edu/provenance-at-harvard/tools) created by the Provenance@Harvard group at Harvard University.