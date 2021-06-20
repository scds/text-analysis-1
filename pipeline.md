---
layout: default
title: An Overview of the Textual Data Analysis Workflow
parent: Lesson
nav_order: 1
---

# An Overview of the Textual Data Analysis Workflow
<br />

When performing textual analysis through computational means, we are working with texts as data. Texts, in their unstructured form - and especially if they have been digitized as an image from a physical source - can only be operated upon by a computer in limited ways. Datafied, or transformed into data amenable to the tasks and operations we can perform with a computer allows for new approaches to understanding texts. As [Thomas Padilla explains](https://labs.loc.gov/static/labs/work/reports/tpadilla_OnaCollectionsasDataImperative_final.pdf), "if the notion of a single digitized text is shifted from a surrogate of a bound paper object to consider the possibility latent in a form that is computationally processable at the level of thousands or even  millions of texts, a move is made toward meaning making that engages affordances unique to data" (Padilla, 1). 

We will become more familiar with what is involved in transforming texts into data later in the lesson, but it is important to note that each transformation involves a layer of interpretation.

> ***Loaded Lingo***

> *When working with data, you may notice the use of metaphorical language that aligns data with unprocessed natural resources like oil or ore. For example, data mining, or raw data or describing the data processing workflow as a pipeline. <br />
> In fact, data are never “raw” – they are always already determined by the choices we make in selecting them and the processes we use to transform them. And while we may use the language of the discipline in order to communicate with other practitioners, it is important to consider how language is used to frame thinking about data in particular ways that are grounded in a colonial paradigm of extraction.*

The textual data analysis workflow below describes the stages of taking textual data from its source - be it a scanned document or born-digital data retrieved from an application programming interface (API) - to . 

Sometimes the order of the steps makes no difference to the end result and sometimes it does – and by “does” we mean that it can result in having to painstakingly redo work that you’ve already completed. Which, of course, we want to avoid.. The graphic below provides an oversimplified overview , with the various stages explained.


\[graphic of workflow]

Acquisition (Input): the text corpus is assembled in a datafied form that can be operated upon computationally. This may involve running optical character recognition (OCR) on scanned physical texts or downloading from an application programming interface (API).

Initial data analysis (IDA): 

Pre-processing:

Exporatory data analysis (EDA):

(Output): 

Of course, the various stages of the workflow may overlap and. When , we may observe characteristics of the data that are sought in the exploratory data analysis phase.

Each stage of the workflow that involves a data transformation (Acquire, Pre-Processing, Output; any data analysis should be performed on a copy of the original dataset to avoid unintentionally transforming the data) holds the potential to introduce errors that often have consequences for later stages of the workflow, which may not become evident until you actually arrive at that stage. It is therefore important to document the transformations you perform so that errors can be traced back and corrected. This documentation also contributes to the record of  creation, or its **data provenance**.


Next -> [Data Provenance](provenance.html)
