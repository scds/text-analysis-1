---
layout: default
title: Pre-Processing Born-Digital Texts
nav_order: 6
---

# Pre-Processing Born-Digital Texts

Not all pre-processing of text data involves correcting OCR errors: working with text created in a digital format presents an entirely different set of challenges.

Analyzing born-digital text data - extracted from PDFs, websites, social media platforms and so on - may instead require you to exclude dozens or even hundreds of other data points, change encodings, convert HTML entities, normalize values and more.

Although writing a program in Python or R will accomplish some tasks more efficiently, OpenRefine is still incredibly useful when pre-processing born-digital text data as well. OpenRefine accepts JSON files, a format that many application programming interfaces (APIs) output, in addition to line-based text files that we have already worked with. Much of what you learned in the lesson on pre-processing digitized texts will have applications for born-digital text data, like splitting cells and isolating rows to limit the scope of your transformations.

A few additional features of OpenRefine may assist your pre-processing of born-digital text data:

## Removing columns

If your data source outputs fields (features) that are not relevant to your analysis, you can remove columns using the "All" column menu: `Edit columns` > `Reorder / remove columns`.

It may be more efficient to use a programmatic approach if you have a large number of rows to remove.

## Transpose rows across columns

Just as we can remove columns, we can also add them based on existing cell contents; for example, objects with multiple properties or strings containing more than one value (e.g. LastName, FirstName).

Go to the column menu of the column you would like to split: `Edit columns` > `Split into several columns...`.

Choose a column separator to split the column on (e.g. comma); you can use regular expressions as well. Leave the "Split into _______ columns at most" blank if you are not sure how many times the separator will occur in the cells - you can always undo if you unexpected end up with dozens of rows!

## Clustering similar cells

Sometimes (human-made) spelling errors can interfere with data analysis as well. Clustering is useful when there are small variances between similar values, such as typos, differences in case or punctuation. OpenRefine will treat "Ammonia" and "ammonia" as distinct values.

You can access clustering from the column menu: `Edit cells` > `Cluster and edit...`.

OpenRefine will present you with groups of very similar values. You can choose to merge them to normalize the values.

The above image shows a


. You may wish to narrow down your 




