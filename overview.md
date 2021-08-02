---
layout: default
title: An Overview of the Textual Data Analysis Workflow
parent: Lesson
nav_order: 1
---

# An Overview of the Textual Data Analysis Workflow
<br />

When performing textual analysis through computational means, we are working with texts as data. Texts, in their unstructured form - and especially if they have been digitized as an image from a physical source - can only be operated upon by a computer in limited ways. Datafied, or transformed into data that is amenable to the tasks and operations we can perform with a computer, allows for new approaches to understanding texts. As [Thomas Padilla explains](https://labs.loc.gov/static/labs/work/reports/tpadilla_OnaCollectionsasDataImperative_final.pdf), "if the notion of a single digitized text is shifted from a surrogate of a bound paper object to consider the possibility latent in a form that is computationally processable at the level of thousands or even  millions of texts, a move is made toward meaning making that engages affordances unique to data" (Padilla, 1). 

We will become more familiar with what is involved in transforming texts into data later in the lesson, but it is important to note that each transformation involves a layer of interpretation. And each layer of interpretation opens up the possibility for different forms of bias - such as a system trained only on texts written by white European authors - to enter in.

The textual data analysis workflow below describes the stages of taking textual data from its source - be it a scanned document or born-digital data retrieved from an application programming interface (API) - to an output from a computational process. It is a simiplified overview; each stage will be articulated as a series of tasks that vary depending on the project.

\[graphic of workflow]

Acquisition/Input: the text corpus is assembled in a datafied form that can be operated upon computationally. This may involve running optical character recognition (OCR) on scanned physical texts or downloading from an API.

Initial data analysis (IDA): in the initial data analysis stage, we are attending to potential errors in the data for the most part; that is, to identify features of the data that may impact how we work with it and to inform the steps of the pre-processing stage. Numerous tools exist to support IDA, depending on the type of data you are working with and the kinds of errors you are trying to find. Even ; in the lesson that follows, we use a ubiquitous word processing software to perform IDA (with a little help from a macro). 

Pre-processing:

Exporatory data analysis (EDA): in the second round of data analysis, we make and test inferences about the data.

Dissemination/Output: communicating findings from the exploratory data analysis process, which may. 

> ***Loaded Lingo***

> *You may notice the use of metaphorical language that aligns data with unprocessed natural resources like oil or ore. For example, data mining or raw data or describing the data processing workflow as a pipeline. <br /><br />
> In fact, data are never “raw” – they are always already determined by the choices we make in selecting them and the processes we use to transform them. And while we may use the language of the discipline in order to communicate with other practitioners, it is important to consider how language is used to frame thinking about data in particular ways that are grounded in a colonial paradigm of extraction.*

Of course, the various stages of the workflow may overlap and occur out of sequence. When we are doing out initial data analysis, we are likely to observe characteristics of the data that are sought in the exploratory data analysis phase. The order of the stages is important, however

In the current lesson, we will focus on the second and third stages – initial data analysis and pre-processing - to prepare the text for computational analysis, which will be the focus of the lessons that follow. The pre-processing step is often overlooked can amount to 70% of the labour ; it is unglamourous work but it 

Each stage of the workflow that involves a data transformation (Acquire, Pre-Processing, Output; any data analysis should be performed on a copy of the original dataset to avoid unintentionally transforming the data) holds the potential to introduce errors that often have consequences for later stages of the workflow, which may not become evident until you actually arrive at that stage. It is therefore important to document the transformations you perform so that errors can be traced back and corrected. This documentation also contributes to the record of its origins, or its **data provenance**.


Next -> [Data Provenance](data-provenance.html)
