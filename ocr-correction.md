---
layout: default
title: Correcting OCR Errors
parent: Lesson
nav_order: 4
---

# Correcting OCR Errors with OpenRefine

Correcting OCR Errors is a significant dimension of the data pre-processing stage when working with scanned documents that have had optical character recognition performed on them.

Presently, the only way to achieve 100% accuracy with OCR text output is to manually correct each misspelled word. If your purposes can allow for some margin of error, however, the trade-offs of time vs accuracy afforded by automated approaches are worthwhile. Numerous tools and strategies exist, requiring various levels of programming expertise. 

In the lesson that follows, we use OpenRefine - a spreadsheet-like software - to assist with identifying and correcting errors (i.e. still requires human ingenuity, but warp-powered).

> *There is no need to worry about overwriting your data in the event that you accidentally introduce new errors while correcting the existing ones (provided that you discover them!): OpenRefine works on a copy of your data rather than directly on the original file. And it shows a history of your transformations so you can easily narrow in on the step you want to undo.*  

> ***Errors in Large Text Corpora***

> *Because many computational analysis methods for texts ultimately involve counting words, a misspelling here or there is not likely to impact your results significantly. Or if an error is consistent, it will become evident in the exploratory data analysis phase. It is important to acknowledge the limitations of not thoroughly correcting errors in the source texts, however.*


## Now, With Your Own Data...

The following lesson will be demonstrated with a sample corpus, which you may wish to use initially to become familiar with the workflow tasks. Then, reinforce and build upon your learning by replicating the steps you completed in the videos using the sample corpus with your own data.

Recall that you will probably be working with a subset of your entire corpus to start with, unless your corpus is already relatively small - and a subset that is hopefully representative of the larger whole. When working with your own data, you will find that it has idiosyncratic features which require you to design your own workflow or improvise other error correction strategies not discussed in the lesson. Computational text analysis is definitely a skill you learn by doing, and working with numerous distinct corpora will help to enrich your understanding of it.

### STEP 1: Import your texts

\[video]

Begin by opening OpenRefine; it will open in your default web browser and prompt you to create a project. Click or tap on the "Browse..." button to locate your text files. OpenRefine will allow you to upload .txt files, treating each line of the text document as a new row.

Import options:
* Store blank rows - OpenRefine has a ceiling on the number of rows you can work with, so uncheck to exclude blank rows 
* Store file source (if using multiple documents) - if you wish to "re-constitute" your documents later (i.e. output them as separate documents), leave checked 

Give your project a name and Create Project >>

### STEP 2: Initial Data Analysis

The first time you upload your text files to OpenRefine, you will likely learn something new about how they are structured - e.g. where line breaks occur or how characters might be interpreted differently in OpenRefine from the text editor you used for any earlier initial data analysis. This can have consequences for the pre-processing steps you undertake, so take some time to review the data in OpenRefine before performing any transformations. You may discover that you need to do some pre-processing tasks with the .txt files in a text editor before re-uploading them to OpenRefine.

For example, longer words in newspapers and other texts will frequently be split over two lines separated with a hyphen or dash - 

### STEP 3: Tokenize

Tokenization - in the context of computational text analysis - is the splitting of unstructured text into individual words, or *tokens*. Because OpenRefine works most effectively with tabular data (i.e. data stored in tables, like in a spreadsheet), we are artificially creating a tabular structure by putting each word on its own row. This achieves the same effect as tokenization and allows us to group identical or similar words in OpenRefine.

Split column We will use the and . Although we can probably think of cases in which a space does not indicate a new word, .  

For now, we will leave in punctuation. Computational text analysis tools will typically remove the punctuation for us, and we may want the punctuation to remain if we are exporting a copy. Bear in mind that OpenRefine will view "elephant" and "elephant." as two distinct entities, however. 

### STEP 3: Remove blank rows and whitespaces

Remove blank rows - Blank rows are not relevant to our error correction tasks in OpenRefine and

Remove trailing whitespaces - reduces the likelihood that , but think through before doing.

### STRATEGY: Find-and-Replace

Fro

Find-and-replace is at the heart of the other post-OCR error correction strategies discussed in the lesson.

### STRATEGY: Regular Expressions (RegEx)

### STRATEGY: Cluster and Edit




