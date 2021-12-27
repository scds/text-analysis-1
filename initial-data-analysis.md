---
layout: default
title: Initial Data Analysis
parent: Lesson
nav_order: 3
---

# Initial Data Analysis

Initial data analysis (IDA) is performed early in the textual analysis workflow in order to better understand the reliability and completeness of the data. It may be done with a number of tools, such as text editors and visualization software like [Voyant](https://voyant-tools.org/). In the lesson that follows, we will use Microsoft Word to perform initial data analysis given its available functionality and ubiquity; [Apache OpenOffice](https://www.openoffice.org/download/index.html) is an open-source alternative if you do not have access to MS Word.

Initial data analysis gives us a sense of the errors that exist within the corpus, but also informs the design of your pre-processing workflow: in what order should the error correction steps take place? What potential new errors may be introduced by an error correction strategy that is too broad (e.g. replacing "m" with "in" because "in" is sometimes misinterpreted as "m")? What tasks can be streamlined? You may, for example, decide that you should group similar documents together to efficiently pre-process them. 

For example, if you notice that errors in the document tend to be consistent and few in number (i.e. 95-99% accuracy) then using OpenRefine may be a feasible approach to automate some of the tasks while retaining greater control over the corrections that occur. A higher number of unpredictable errors may require using a machine learning system that you train yourself. 

## Initial Data Analysis (IDA) and Exploratory Data Analysis (EDA)

Typically, initial data analysis informs the pre-processing stage while exploratory data analysis concerns testing hypotheses and identifying salient features of the data to communicate in the output stage.

The two are not neatly separated; you are likely to notice some features and characteristics of the data as you are performing your initial data analysis. But generally, exploratory data analysis will largely occur in the later stages of the workflow when we are performing natural language processing tasks such as named entity recognition and topic modelling.

## Performing Initial Data Analysis with Microsoft Word

VIDEO

Working with [sample corpus A](https://scds.github.io/text-analysis-1/preparation.html), open the .txt file in MS Word. We are using Word because it will highlight errors for us and we can export a list of misspelled words from it using a macro. 

The software, however, may not recognize errors automatically when working with a .txt file. If you are running MS Word on either a Windows or Mac operating system, you can ^^^ under the "Review" spell check tool on your .txt file.

Once you have made spelling errors visible in your document, take some time to review them - they are now easy to find! Although we are about to export a list of misspelled words, it is helpful to see the errors in context as it can at times be difficult to infer the correct spelling of the error without knowing how they are being used.

In your initial data analysis, try to identify patterns within the errors:
* is one character frequently the source of errors (such as "m" in the sample text)?
* is one or a set of characters regularly substituted for another ("oim" for "oun" in the sample text)?
* does an error often occur in relation to another character or characters (like "m" for "in" when following "f" or "tiy" for "tly" in the sample text)?
* etc.

Document your observations as completely as possible to help to make your error correction tasks more efficient and less likely to introduce new errors. 

### Create a Macro to Export an OCR Error List

Although seeing the errors in context is helpful, it is of course also useful to isolate the errors. We can create a list of OCR errors using a macro in MS Word.

With the Zwick.txt file open, go to the Macros in MS Word.

Copy the macro code from the , written by Allan Wyatt (https://word.tips.net/T001465_Pulling_Out_Spelling_Errors.html)).

If you are using OpenOffice, you should be able to similarly [create a macro using the same code](https://wiki.openoffice.org/wiki/Documentation/OOoAuthors_User_Manual/Getting_Started/Creating_a_simple_macro).

In [Correcting OCR Errors with OpenRefine](https://scds.github.io/text-analysis-1/ocr-correction.html), we will use the "Word Facet" option in OpenRefine to group the same misspellings together so that each error only appears once in the list.

Next -> [Correcting OCR Errors with OpenRefine](https://scds.github.io/text-analysis-1/ocr-correction.html)
