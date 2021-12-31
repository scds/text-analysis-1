---
layout: default
title: Correcting OCR Errors with OpenRefine
parent: Lesson
nav_order: 4
---

# Correcting OCR Errors with OpenRefine

Correcting OCR Errors is usually the largest task of the data pre-processing stage when working with scanned documents that have had optical character recognition performed on them.

Presently, the only way to achieve 100% accuracy with OCR text output is to manually correct each misspelled word. If your purposes can allow for some margin of error, however, the trade-offs of time vs accuracy afforded by automated approaches are worthwhile. Numerous tools and strategies exist, requiring various levels of programming expertise. 

In the lesson that follows, we use OpenRefine - a spreadsheet-like software - to assist with identifying and correcting errors (i.e. still requires human ingenuity, but warp-powered).

There is no need to worry about overwriting your data in the event that you accidentally introduce new errors while correcting the existing ones (provided that you discover them!): OpenRefine works on a copy of your data rather than directly on the original file. And it shows a history of your transformations so you can easily narrow in on the step you want to undo.  

> ***Errors in Large Text Corpora***

> *Because many computational analysis methods for texts ultimately involve counting or classifying words, a misspelling here or there is not likely to impact your results significantly if a word occurs frequently. Or if an error is significant and consistent, it will likely become evident in the exploratory data analysis phase. It is important to acknowledge the limitations of not thoroughly correcting errors in the source texts, however.*

## Limitations of OpenRefine

OpenRefine is not a purpose-built tool for correcting OCR errors, but it can be used... creatively. There will be text analysis projects for which OpenRefine is a viable approach to error correction and others for which it is not.

The techniques demonstrated in the current lesson work best with high quality scans of typewritten documents, such as reports, typed correspondence, book pages, journal articles and so on. Documents with relatively few, consistently-occurring errors after OCR is performed. 

You may also wish to use OpenRefine if you are already familiar with it and / or new to writing code. If you are comfortable working in Python or willing to learn, you might find the [OCR Error Correction with Python tutorial](advanced-correction.html) more suitable for your needs. 

You may also have to use Python if you are working with handwritten documents or other texts with many unique errors following OCR. From the IDA stage, you should have a sense of whether to a programmatic approach is more appropriate.

## Using OpenRefine to correct OCR errors

The following lesson will be demonstrated with [sample corpus A](preparation.html), which you may wish to use initially to become familiar with the workflow tasks. Then, reinforce and build upon your learning by replicating the steps you completed in the videos using your own data.

You will probably be working with a subset of your entire corpus to start with, unless your corpus is already relatively small - and a subset that is hopefully representative of the larger whole. When working with your own data, you will find that it has idiosyncratic features which require you to design your own workflow or improvise other error correction strategies not discussed in the lesson. Computational text analysis is definitely a skill you learn by doing, and working with numerous distinct corpora will help to enrich your understanding of it.

### Overview of tasks

Using OpenRefine to correct OCR errors involves:
1. Importing your text file(s)
2. Breaking down the unstructured text into words that we can operate on individually (tokenization) 
3. Correcting individual words using a variety of find-and-replace strategies
4. "Reconstituting" the words into a text file that can be used for computation analysis or another purpose

Next -> [Correcting OCR Errors with OpenRefine: Preparing the Data](or-prep.html)
