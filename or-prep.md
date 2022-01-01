---
layout: default
title: Preparing the Data in OpenRefine
parent: Lesson
nav_order: 5
---
# Correcting OCR Errors with OpenRefine: Preparing the Data

## OpenRefine step 1: Import your texts

\[video]

Begin by opening OpenRefine; it will open in your default web browser and prompt you to create a project. Use the `Browse...` button to locate your text files. OpenRefine will allow you to upload .txt files, treating each line of the text document as a new row.

\[screenshot]

Import options:
* Store blank rows - leave checked if you want to preserve the paragraph structure of the document; otherwise uncheck*
* Store file source (if using multiple documents) - if you wish to "reconstitute" your documents later (i.e. output them as separate documents), leave checked 

\**OpenRefine has a ceiling on the number of rows you can work with (~1,000,000) so you may wish to conserve resources by excluding blank rows.*

Give your project a name and `Create Project >>` to open your document(s) in OpenRefine.

## OpenRefine step 2: Initial Data Analysis

Although you will already have done much of your initial data analysis in another tool, you will often learn something new about how your text files are structured when you upload them to OpenRefine - e.g. where line breaks occur or how characters might be interpreted differently in OpenRefine from the text editor you used for any earlier initial data analysis. There can be consequences for the pre-processing steps you undertake, so take some time to review the data in OpenRefine before performing any transformations. You may discover that you need to do some pre-processing tasks with the .txt files in a text editor before re-uploading them to OpenRefine.

For example, longer words in newspapers and other justified typeset documents will sometimes be split over two lines separated with a hyphen or dash - it is usually easier to reconnect them in a text editor like TextEdit or Notepad++ before uploading to OpenRefine using a find-and-replace function in the editor (make a copy of your data first, as it is a destructive edit).

Once you have performed any additional (pre-)pre-processing steps outside of OpenRefine and re-uploaded your text file(s), rename the column with the contents of your text "Tokens" by visiting the column menu - which can be accessed through the small downward arrow to the left of the column - and selecting `Edit column > Rename`.

\[screenshot of expanded menu and renamed column]

### Optional: Paragraph placeholders

\[video]

If the original paragraph structure of the document is significant your intended use of the text data (e.g. for readability, stylometric analysis), there is another step that must be performed before tokenizing the data. We can maintain the paragraph structure of a document in the output from our error correction in OpenRefine, but it takes an additional step early on in the workflow - before we break the sentences into tokens in the next step.

Provided you left "Store blank rows" checked when importing the document, each blank - or null - row in the data represents a line break. Replace the null rows with a placeholder character that you can later use to replace with a new line.

Create a facet - or grouping of rows with the same contents - that contains all of the null rows by going back to the dropdown menu, `Facet > Customized facets > Facet by null`. 

\[screenshot of facet]

Filter the rows to show null values only by selecting "Include" from the facet menu next to "True" (i.e. those rows that contain null values). With the null values isolated, we can now perform a replace action to fill each blank row with a placeholder character.

Hover over any of the rows and you will notice that an "Edit" message appears, allowing you to edit individual cells. In the cell that you edit, enter a placeholder character and select the "Apply to All Identical Cells" (`ctrl` / `cmd` + `Enter`) option to transform all null rows.

\[screenshot of edit row]

Choose a placeholder character that does not exist anywhere else in the text, as you will be performing a find-and-replace action later to substitute a line break for the placeholder. We recommend using the HTML tag for paragraph, or `<p></p>`, which will preserve the paragraph structure without any additional actions if the text is output to HTML. Copy the code exactly as it is below:

`</p><p>`

(The order of the markup tags is reversed so that each blank row closes the previous paragraph tag and opens a new one around the content that follows.)

\[screenshot of paragraph tag replacing all]

Once the null rows have been transformed, they should no longer be visible as their value are no longer null. Remove the facet by closing it, and all rows will return. As we tokenize the data in the next step, the placeholders will be treated as another token and preserved for later use to restored the paragraph structure of the text.

### OpenRefine step 3: Tokenize

Tokenization - in the context of computational text analysis - is the dividing of unstructured text into individual words, or *tokens*. Because OpenRefine works most effectively with tabular data (i.e. data stored in tables, like in a spreadsheet), we are artificially creating a tabular structure by putting each word on its own row. This achieves the same effect as tokenization and allows us to group identical or similar words in OpenRefine.

In the "Tokens" column of your OpenRefine file, open the column menu using the small downward arrow to the left of the column title. From the column menu, select Edit cells > Split multi-valued cells....

\[screenshot]

By default, the recommended separator character will be a comma (i.e. for comma-separated value, or CSV, files) - delete the comma and hit the space bar once to specify the space character as the separator. We are indicating to OpenRefine to split each cell every time it encounters a space in the text. Although we can think of cases in which a space does not indicate a new word, we will be putting the text back together again with the spaces restored when we have finished with error correction.  

\[screenshot]

For now, we will leave in punctuation. Computational text analysis tools will typically remove the punctuation for us, and we may want the punctuation to remain if we are exporting a copy. Bear in mind that OpenRefine will view "bananas" and "bananas!" as two distinct entities, however. 

> *You can optionally split any punctuation into its own cell to simplify error correction by repeating the steps above using the separator ^^^ with ^^^regex checked off. But you may not wish to if you intend to "reconstitute" the text for purposes other than computational analysis (i.e. to provide a corrected copy of the text to users). When we recombine the text, we will use a space to separate each cell (word) - meaning there will be a space in front of all punctuation marks.
> 
> Much of OCR error correction, and data pre-processing in general, is being able to consider the entire data analysis workflow and to anticipate ^^^.*
  
You can also use filters to help with your analysis by going to the dropdown menu for the column (which I have renamed "Tokens" in the screenshot below) and selecting "Edit Ce; for example, many errors in the Zwick.txt document involved the letter "m" so you could filter by m (case-sensitive checked). Such a broad **word** or **text facets** 


### OpenRefine step 4: Remove blank rows (and whitespaces)

Much like punctuation, whitespaces in front of or behind a word will prevent it from being grouped with other instances of the same word in OpenRefine. Although there are ways to normalize the data in OpenRefine through the "Cluster and Edit" function, we can easily remove them using the "Remove leading and trailing whitespaces" function.

\[video: Remove whitespaces and blank rows]

**To remove whitespaces**, open the "Tokens" column menu from the previous step and select Edit cells → Commons transforms → Trim leading and trailing whitespace. Once you have done so, OpenRefine will report how many cells were transformed.

\[screenshot]

It is possible that no rows will be affected by removing leading and trailing whitespaces, unless additional spaces erroneously appear in the text (i.e. two spaces where there ought to be one). It is nonetheless good practice to ensure that we are indeed comparing like with like!

Optionally, you may also wish to remove blank rows in the dataset. Blank rows are not relevant to our error correction tasks in OpenRefine and, as OpenRefine does have a ceiling on the number of rows it can work with, you may wish to delete. On the other hand, if you want to preserve the formatting in your output - that is, preserve the line breaks in the document you export - then you can leave them in.

**To remove blank rows**, go to Edit cells → Facet → Customized facets → Facet by blank (null or empty string).

\[screenshot]

From the facet that is created, include “True” which temporarily exclude any cells that are not blank. Star any of the rows that remain (they will all be blank cells).

\[screenshot]

Here, instead of the "Tokens" column, we will use the menu in the "All" column to the left of it: All → Edit rows → Remove matching rows. It will remove all of the rows that match; that is, all of the blank rows.

\[screenshot]

Next -> [Correcting OCR Errors with OpenRefine: Strategies](or-strat.html)

