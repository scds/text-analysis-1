---
layout: default
title: Strategies for OCR Error Correction in OpenRefine
parent: Correcting OCR Errors with OpenRefine
grand_parent: Lessons
nav_order: 2
---

{: .no_toc }
# 3. Strategies for OCR Error Correction in OpenRefine

## Lesson Video
The following video demonstrates each of the steps outlined below in text.
<iframe id="kmsembed-1_xo1h3x4i" width="100%" height="416" src="https://www.macvideo.ca/embed/secure/iframe/entryId/1_xo1h3x4i/uiConfId/39241881" class="kmsembed" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" referrerPolicy="no-referrer-when-downgrade" sandbox="allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" frameborder="0" title="Kaltura Player"></iframe>

In the next part of the lesson, we will explore several strategies you can use in OpenRefine to correct errors produced through optical character recognition more efficiently than replacing individual words. Together, they form the basis for a unique error correction program that OpenRefine helps you to write - as we will learn in [Exporting your Data](output.html). 

Though still a manual process of creating find-and-replace commands, the corrections you make are likely to be (far) more accurate than a machine learning approach (for the time being).

<div markdown="1" style="border: 1px solid #7a003c; border-radius: 6px; margin-bottom: 1em; padding: 0.5em 1em 0; margin-top: 1em;" class="toc">
<summary style="cursor:default; display: block; border-bottom: 1px solid #302d36; margin-bottom: 0.5em">
  Jump to step >
</summary>
- [3.1. Find-and-replace with text filters](#step1)
- [3.2. Find-and-replace with GREL (Google / General Refine Expression Language)](#step2)
- [3.3. Find-and-replace with regular expressions (RegEx)](#step3)
</div>

## 3.1. Find-and-replace with text filters {#step1}
<iframe id="kmsembed-1_8f8gstrm" width="100%" height="416" src="https://www.macvideo.ca/embed/secure/iframe/entryId/1_8f8gstrm/uiConfId/39241881" class="kmsembed" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" referrerPolicy="no-referrer-when-downgrade" sandbox="allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" frameborder="0" title="Kaltura Player"></iframe>

Find-and-replace is at the heart of the other OCR error correction strategies discussed in the lesson. While find-and-replace commands can automate error correction to some extent, it can also lead to the introduction of new errors if not applied precisely. Text filters in OpenRefine allow us to apply find-and-replace transformations in a targeted manner. 

We used text filters for initial data analysis in OpenRefine; here, we will employ them to limit the scope of our transformations.

Try it out by going to the "Tokens" column menu, selecting `Text filter` and searching "no" (with case-sensitive checked). Create a word facet to group your results.

Include "Ontano" and "vanous" to omit the other results, which are not misspelled. From the "Tokens" column menu again, select `Edit cells` > `Replace` to open a dialog box. 

<img src="../assets/img/strategy/strategy_replace-1.png" width="100%" alt="" style="border: solid 2px black">

Type "no" in "Find: " and "rio" in "Replace: " - we use "no" instead of "n" because our actions would transform "Ontano" into "Oritario." 

<img src="../assets/img/strategy/strategy_replace-2.png" width="100%" alt="" style="border: solid 2px black">

If you notice that you have made an error, you can easily undo it by going to the "Undo / Redo" tab. Before working through your error list with "Replace," however, there is an alternative – and arguably better – approach. Read on...

## 3.2. Find-and-replace with GREL (Google / General Refine Expression Language) {#step2}
<iframe id="kmsembed-1_4df746o0" width="100%" height="416" src="https://www.macvideo.ca/embed/secure/iframe/entryId/1_4df746o0/uiConfId/39241881" class="kmsembed" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" referrerPolicy="no-referrer-when-downgrade" sandbox="allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" frameborder="0" title="Kaltura Player"></iframe>

Performing find-and-replace tasks with GREL, or General Refine Expression Language, allows us to use variables and create formulas - we can correct more errors at once while at the same time not being overly broad in the scope of our transformations. Going the GREL route is a preferred strategy to the “replace” command in OpenRefine because you can preview your changes before you apply them.

To use GREL in OpenRefine, go to the "Tokens" column menu and select `Edit cells` > `Transform` to open the custom text transform box that gives us access to the GREL language. We will use the function `value.replace(a, b)` in the “Expression” box to apply a replace transformation, where *a* is what to replace and *b* is what to replace it with.

<img src="../assets/img/strategy/strategy_transform.png" width="100%" alt="" style="border: solid 2px black">

As in our earlier replace actions, start by filtering rows to limit the extent of our transformations. Practice with “oim” - which we know has replaced “oun” in numerous words.

In the custom text transform box, type `value.replace(“oim”, “oun”)` exactly - remember to include the quotations marks around the letters to indicate that we are working with text strings and not numbers or other data types. A preview will show you the results of your transformation. 

<img src="../assets/img/strategy/strategy_grel.png" width="75%" alt="" style="border: solid 2px black">

After you have applied the tranformation, OpenRefine will notify you that 15 rows have been changed and you should no longer have any rows visible (because they will no longer contain "oim"). You can either close the filter to remove it or clear its contents to return all rows.

There are other functions that might be useful to your OCR error correction efforts if you would like to read over the [reference for GREL](https://docs.openrefine.org/manual/grelfunctions) in greater depth.

## 3.3. Find-and-replace with regular expressions (RegEx) {#step3}
<iframe id="kmsembed-1_eb68oxh5" width="100%" height="416" src="https://www.macvideo.ca/embed/secure/iframe/entryId/1_eb68oxh5/uiConfId/39241881" class="kmsembed" allowfullscreen webkitallowfullscreen mozAllowFullScreen allow="autoplay *; fullscreen *; encrypted-media *" referrerPolicy="no-referrer-when-downgrade" sandbox="allow-forms allow-same-origin allow-scripts allow-top-navigation allow-pointer-lock allow-popups allow-modals allow-orientation-lock allow-popups-to-escape-sandbox allow-presentation allow-top-navigation-by-user-activation" frameborder="0" title="Kaltura Player"></iframe>

We can build on our find-and-replace toolkit by incorporating regular expressions, or RegEx, which offer a way to search for more generalized patterns when we may not know or be able to articulate specifics. For example, performing a search that all results ending in “mg” regardless of what comes before. 

Combined with GREL transformations, filters and facets, we can achieve a balance between speeding up our OCR error efforts while not being so inclusive that we introduce new errors.

To get a sense of RegEx in OpenRefine, create a text filter with "mg" as the criteria to find words where "ing" has been misinterpreted by the OCR engine. Note that, in addition to the words we would like to change, there are a number of correctly spelled results (i.e. "mg/L").

<img src="../assets/img/strategy/strategy_mg-filter.png" width="60%" alt="" style="border: solid 2px black">

To limit the scope to rows (words) that end in "mg" we can use the regular expression "$mg" as the filter criteria, ensuring that the "regular expression" box is checked. We can now proceed with our text transformation without affecting correctly spelled words.

<img src="../assets/img/strategy/strategy_regex.png" width="100%" alt="" style="border: solid 2px black">

### Quick RegEx Reference

Other RegEx patterns you might find useful to your OCR error correction efforts include: 

<div class="code-example" markdown="1">
`^` - start of expression  
`$` - end of expression

E.g.
`^T$` will only return cells with “T”  
`^mn` will only return cells that start with “mn”  
`ent$` will only return cells that end with “ent” 
</div>

<div class="code-example" markdown="1">
`[string]` - contains any of the letters  
`[^string]` - does not contain the letters

E.g.  
`[iou]m` will return words that contain “im,” “om” and “um”  
`ti[^o]` will exclude “tion”
</div>

Familiarity with RegEx will improve your ability to correct OCR errors in OpenRefine considerably; you can seek out other patterns by consulting RegEx references like the [Mozilla RegEx cheatsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet) or [RegEx One tutorials](https://regexone.com/).

## Try it with your own data...

By now, you can likely appreciate how the specific transformations we have made on the Zwick.txt dataset are highly context-dependent. Each corpus will entail a unique set of tranformations to correct the OCR errors within.

With your own dataset, try out the strategies above to correct 5 to 10 error patterns in your corpus before moving on to the next step of the lesson wherein we will export our data from OpenRefine to a text format.

## Key Points / Summary
* Using GREL is preferred over the "replace" command in OpenRefine
* RegEx allows you to do more powerful and specific search queries
