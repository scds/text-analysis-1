---
layout: default
title: Strategies for OCR Error Correction in OpenRefine
parent: Lesson
nav_order: 6
---
# Correcting OCR Errors with OpenRefine: Strategies

\[video]

In the next part of the lesson, we will explore severals strategies you can use in OpenRefine to correct errors produced through optical character recognition more efficiently than replacing individual words. Together, they form the basis for a unique error correction program that OpenRefine helps you to write - as we will learn in [Exporting your Data](output.html). 

Though still a manual process of creating find-and-replace commands, the corrections you make are likely to be (far) more accurate than a machine learning approach (for the time being).

## Strategy 1: Find-and-replace with text filters

\[video]

Find-and-replace is at the heart of the other OCR error correction strategies discussed in the lesson. While find-and-replace commands can automate error correction to some extent, it can also lead to the introduction of new errors if not applied precisely. Text filters in OpenRefine allow us to apply find-and-replace transformations in a targeted manner. 

We used text filters for initial data analysis in OpenRefine; here, we will employ them to limit the scope of our transformations.

Try it out by going to the "Tokens" column menu, selecting `Text filter` and searching "no" (with case-sensitive checked). Create a word facet to group your results.

Include "Ontano" and "vanous" to omit the other results, which are not misspelled. From the "Tokens" column menu again, select `Edit cells` > `Replace` to open a dialog box. Type "no" in "Find: " and "rio" in "Replace: " - we use "no" instead of "n" because our actions would transform "Ontano" into "Oritario." 

Before working through your error list with "Replace," however, there is an alternative - and arguably better - approach. Read on...

## Strategy 2: Find-and-replace with GREL (Google / General Refine Expression Language)

\[video]

Performing find-and-replace tasks with GREL, or General Refine Expression Language, allows us to use variables and create formulas so that we can correct more errors at once while at the same time not being overly broad in the scope of our transformations. Going the GREL route is a preferred strategy to the “replace” command in OpenRefine because you can preview your changes before you apply them.

To use GREL in OpenRefine, go to the "Tokens" column menu and select `Edit cells` > `Transform` to open the custom text transform box that gives us access to the GREL language. We will use the function `value.replace(a, b)` in the “Expression” box to apply a replace transformation, where *a* is what to replace and *b* is what to replace it with.

As in our earlier replace actions, start by filtering rows to limit the extent of our transformations. Practice with “oim” - which we know has replaced “oun” in numerous words.

In the custom text transform box, type `value.replace(“oim”, “oun”)` exactly - remember to include the quotations marks around the letters to indicate that we are working with text strings and not numbers or other data types. A preview will show you the results of your transformation. After you have applied the tranformation, OpenRefine will notify you that 15 rows have been changed and you should no longer have any rows visible (because they will no longer contain "oim"). You can either close the filter to remove it or clear its contents to return all rows.

There are other functions that might be useful to your OCR error correction efforts if you would like to read over the [reference for GREL](https://docs.openrefine.org/manual/grelfunctions) in greater depth.

## Strategy 3: Find-and-replace with regular expressions (RegEx)

We can build on our find-and-replace toolkit by incorporating regular expressions, or matching sequences of characters.


## Try it with your own data...

You can likely appreciate how context-dependent the specific transformations we have made are. Unique combinations of 

Next -> [Exporting your Data](output.html)
