---
layout: default
title: Correcting OCR Errors
parent: Post-OCR Error Correction
nav_order: 4
---

# Correcting OCR Errors

Correcting OCR Errors is a facet of the data pre-processing stage, commonly required when working with scanned documents that have had optical character recognition performed on them.

At present, the only way to achieve 100% accuracy with OCR text output is to manually correct each misspelled word. If your purposes can allow for some margin of error, however, the trade-offs of time for accuracy afforded by automated approaches are worthwhile. Numerous tools and strategies exist, requiring various levels of programming expertise. In the lesson that follows, we use OpenRefine - a spreadsheet-like software - to assist with identifying and correcting errors (i.e. still requires human ingenuity, but warp-powered).

> ***Errors in Large Text Corpora***

> *Because many computational analysis methods for texts ultimately involve counting words, a misspelling here or there is not likely to impact your results significantly. Or if an error is consistent, it will become evident in the exploratory data analysis phase. It is important to acknowledge the limitations of not thoroughly correcting errors in the source texts, however.*

VIDEO HERE

The video goes through the steps of the lesson using the sample corpus provided on the [Preparation](/preparation.html) page. If you prefer written instructions to a video lesson, follow the steps and strategies in the section below with the sample corpus.

# Now, With Your Own Data...

Reinforce and extend your learning by replicating the steps you completed in the video using the sample corpus with your own data.

Recall that you will probably be working with a subset of your entire corpus to start with, unless your corpus is already relatively small - and a subset that is hopefully representative of the larger whole. When working with your own data, you will find that it has idiosyncratic features which require you to design your own workflow or improvise other error correction strategies not discussed. Computational text analysis is a skill you learn by doing and working with numerous 

## STEP 1: Import your texts

Begin by opening OpenRefine; it will open in your default web browser and prompt you to create a project. Click or tap on the "Browse..." button to locate your text files. OpenRefine will allow you to upload .txt files, treating each line of the text document as a new row.

The first time you upload your text files to OpenRefine, you will likely learn something new about how they are structured - e.g. where line breaks occur or how characters might be interpreted differently in OpenRefine from the text editor you used for initial data analysis. This can have consequences for the pre-processing steps you undertake, so take some time to review the data in OpenRefine before performing any transformations. You may need to do some pre-processing tasks 

## STEP 2: Tokenize

Tokenization is the splitting of unstructured text into . Because OpenRefine, we are artificially . Although we can probably think of cases in which a space does not indicate a new word, . For now, we are also leaving in punctuation.

## STEP 3: Remove blank rows

> ***On the Importance of Initial Data Analysis***
> *Initial data analysis gives us a sense of the errors that exist within the corpus, but also informs the design of your pre-processing workflow: what order should the error correction steps take place? What ? You may, for example, decide that you should group similar documents together before uploading them to OpenRefine. Much of the data pre-processing stage relies on being able to anticipate
> 
> There is no need to worry about making errors  (provided that you discover them!): OpenRefine works on a copy of your data rather than directly on the original file. And it shows a history of your transformations so you can easily narrow in on the step you want to undo.  

## STRATEGY: Find-and-Replace

Fro

Find-and-replace is at the heart of the other post-OCR error correction strategies discussed in the lesson.

## STRATEGY: Regular Expressions (RegEx)

## STRATEGY: Cluster



