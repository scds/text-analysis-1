---
layout: default
title: Preparation
nav_order: 2
---

<!-- Edit the content below for the workshop in question. Once you're ready to publish, remove the comment characters e.g. "<!--" at the start and end -->

# Workshop preparation 

Preparing for the lesson involves:

<!--
## Get the data

The collection of documents we are working with in the lesson were scanned from paper copies and then processed through optical character recognition (OCR) to transform the image into text data. If you would like to read more about how OCR works, read …. 

OCR output is rarely free of errors. The OCR engine may misinterpret characters, even with scanned documents.  The error rate increases when working with handwritten documents that are hand-written, have low contrast between foreground text or are in languages with less robust OCR support (read more at [behind the interface]). 

-->

## Get the software
We will be using [**OpenRefine**](https://www.openrefine.org/), an open-source spreadsheet-like software, for our post-OCR error correction in the lesson. Please download OpenRefine and use the instructions provided to guide you through installation.

[Download OpenRefine](https://openrefine.org/download.html)
[OpenRefine installation instructions](https://docs.openrefine.org/manual/installing)

Please contact the [Sherman Centre](mailto:scds@mcmaster.ca) if you have any difficulties downloading or opening the software.

## Assemble a corpus

In advance of the workshop, we also recommend that you assemble a collection of documents to work with for the *Try it with your data* sections. We will use the text collection, or corpus, provided above to practice the techniques demonstrated in the lesson but each dataset brings its own unique set of challenges. Even if you are not going through the lesson with a specific project in mind, having a different corpus to experiment with will help to reinforce the concepts and enrich your knowledge of the topic.

<!--
Before applying optical character recognition (OCR), you may wish to optimize the quality of your image as will result . Preventing errors earlier in the workflow will save considerable labour later in the .
The lesson uses text files (.txt file extension)
-->

The lesson assumes that your corpus is comprised of a collection of .txt files, which will not always be the case. If you have one long document (like a manuscript), you may find it easier if you create subsets of pages to work with. OpenRefine works best with [fewer than a million rows](https://groups.google.com/g/openrefine/c/-loChQe4CNg/m/eroRAq9_BwAJ); because each word will be its own row, the upper bound of the word count in each subset should be approximately 500,000 - 750,000. But, as that upper bound will depend on a number of resource factors (e.g. available memory), it's best to do a test run before dividing up your entire corpus!


