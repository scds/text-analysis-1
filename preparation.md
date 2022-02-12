---
layout: default
title: Preparation
nav_order: 2
---


# Workshop preparation 
<br />
Preparing for the lesson requires you to:

## 1. Get the data (sample corpus A)
The document we will be working with in the lesson is "[Zwick's Island landfill environmental investigations](https://archive.org/details/zwicksislandland00ontauoft/page/12/mode/2up)," available on the Internet Archive. The report was scanned from a paper version and then processed through [optical character recognition (OCR)](https://archive.org/services/docs/api/ocr.html) to transform the image into text data.

The report describes a study undertaken by the Ontario provincial government's Ministry of the Environment in 1991 about the ongoing environmental impact of the closed Zwick's Island landfill site (the Sherman Centre is located in Ontario, Canada). [A later report](https://www.quinteconservation.ca/en/watershed-management/resources/Documents/ConditionsReport_withAppendices.pdf) prepared by Quinte Conservation indicates that the past land use of the area remains a significant threat to drinking water in surrounding regions (3.10). The landfill site area was built out into the Bay of Quinte, upstream from Tyendinaga Mohawk Territory.

OCR output is rarely free of errors: the OCR engine may misinterpret characters, even with a high quality scan that produces a file that looks like a born-digital PDF.  The error rate increases when working with documents that are hand-written, have low contrast between foreground text or are in languages with less robust OCR support. The "Zwick's Island" document is no exception; like many documents on the Internet Archive and other repositories for digitized texts, access is prioritized over accuracy - meaning that there is an abundance of sources for us to practice with! The accuracy of the post-OCR text of the "Zwick's Island" document is close to an impressive 99%, however. 

Because applying OCR to a scanned document is outside of the scope of the lesson, we are going to work with the post-OCR text: 

1. Go to the [full text version of the document](https://archive.org/stream/zwicksislandland00ontauoft/zwicksislandland00ontauoft_djvu.txt), 
2. Copy the text (ctrl / cmd + A to select all, then ctrl / cmd + C to copy) and,
3. Paste into a text file (create one using Notepad on a Windows OS or TextEdit on a Mac and then ctrl / cmd + V to paste) and save with a .txt extension as Zwick.txt.

**Note that the document is under [Crown copyright](https://www.ontario.ca/page/copyright-information-c-queens-printer-ontario)** (i.e. © Queen’s Printer for Ontario,  1991); please do not reproduce the text outside of your personal use for the purposes of the lesson unless you have determined your use falls under an applicable copyright exception or is otherwise permitted.

## 2. Get the software
We will be using [**OpenRefine**](https://www.openrefine.org/), an open-source spreadsheet-like software, for our post-OCR error correction in the lesson. Please download OpenRefine and use the instructions provided to guide you through installation.

   [Download OpenRefine](https://openrefine.org/download.html)

   [OpenRefine installation instructions](https://docs.openrefine.org/manual/installing)

### Software versions

For the lesson as it is currently written, the software versions are as follows:

**OpenRefine:** 3.5.2

Please contact the [Sherman Centre](mailto:scds@mcmaster.ca) if you have any difficulties downloading or opening the software.

## 3. Assemble your own corpus (optional)
In advance of the workshop, we also recommend that you assemble a collection of documents to work with for the *Try it with your data* sections. We will use the text collection, or corpus, provided above to practice the techniques demonstrated in the lesson but each dataset brings its own unique set of challenges. Even if you are not going through the lesson with a specific project in mind, having a different corpus to experiment with will help to reinforce the concepts and enrich your knowledge of the topic.

Before applying OCR, you may wish to optimize the quality of your image as a clearer image will result in more accurate results. Regardless of the ability to automate some of the tasks, error correction is time-consuming; preventing errors earlier in the workflow will save considerable labour later on. For advice on improving image quality for OCR, consult the guides provided by the [Illinois Library](https://guides.library.illinois.edu/OCR/bestpractices) and [Tesseract](https://tesseract-ocr.github.io/tessdoc/ImproveQuality.html), an open-source OCR engine.

The lesson assumes that your corpus is comprised of a collection of text (.txt file extension) files, which will not always be the case. If you have one long document (like a manuscript), you may find it easier if you create subsets of pages to work with. OpenRefine works best with [fewer than a million rows](https://groups.google.com/g/openrefine/c/-loChQe4CNg/m/eroRAq9_BwAJ); because each word will be its own row, the upper bound of the word count in each subset should be approximately 500,000 - 750,000 words. But, as that upper bound will depend on a number of resource factors (e.g. available memory), it's best to do a test run before dividing up your entire corpus!

Next --> [Pre-Processing Textual Data](instructions.html)
