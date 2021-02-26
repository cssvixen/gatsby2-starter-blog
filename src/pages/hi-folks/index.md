---
title: A beginners look into Specificity
date: "2021-02-26T22:40:32.169Z"
---


Have you ever styled an element with multiple css selectors and only one rule is applied? well this is because of specificity.

Specificity may seem a bit complex for beginners, but understanding this would give you a much clearer concept of how styling works in css and also reduce bug hunting time especially for front-end developers.

So let’s get into this!


<b> What is Specificity? </b>

Specificity is a method by which web browsers choose which css property values are the most relevant to an element and would be applied. It can also be defined as the means by which web browsers use to determine the set of rules applied to a specific selector having two or more conflicting rules.


<b> Specificity Hierachy </b>

Every selector has its place in the hierachy. The higher the weight of the selector, the higher the chance it stands to be applied. In a case where there are two or more css rules applied to the same elements the browser chooses the selector with the highest specificity.


<b> What are selectors? </b>

Selectors help you select the content you want to style. Css selectors select html elements according to their id, class, attribute e.t.c.

The specificity of a selector can be grouped into four distinct categories.


- <b> Inline styles </b>: Css styling is applied directly to html documents. Inline styles have the highest specificity, this means they will be applied no matter what else is dictated in your external stylesheet (with the one exception being any styles that are given the !important declaration that sheet, but this is not something that should be done in production sites if it can be avoided). 


- <b> Ids </b>: Ids like #form have the second highest specificity.


- <b> Classes,pseudo-classes and attributes </b> : They come third place in specificity, examples are .form, :hover, [tittle=”form”] e.t.c.


- <b> Elements and pseudo-elements </b>: They come last and have the least value in specificity examples are <p>, : :firstline e.t.c.


<b> Specificity Rules </b>

Specificity is relatively easy to understand. The weight of selectors is one of the reasons why your css rules dont apply to some elements, although you think they should have.


<b> Rule 1 </b>

If you have the same selector for two or more elements , they will have the same specificity value however the rule that appears below the first on your css file will be applied.

>image here

<b> Rule 2 </b>

If two or more selectors are used for the same element, the selector with the highest specificity will be applied.

>image here


<b> Rule 3 </b>

Contextual selectors are more specific, hence they will be applied rather than single element selectors as in external styling.

> image here


<b> Rule 4 </b>

!important has the ability to override any rule in specificity. However, you should not use !important because it is not considered a good practise in css but you can use when you want to override someone else css.
The only way to override an !important rule is to use another !important rule later in css.

>image here


<b> CALCULATION </b>

Specificty helps you understand how web browsers interprete your code so as to minimize the time for bug hunting.The specificity value can be calculated with the following;


- Inline style : (1,0,0,0)


- Ids : (0,1,0,0)


- Classes and pseudo-classes : (0,0,1,0)


- Elements and pseudo-elements : (0,0,0,1)


<b> CONCLUSION </b>

So, we have been able to see and understand how specificity works and the concepts behind it, from the hierarchy, to the rules to the calculations. This tool is very important for front-end developers as it enables minimisation of bug hunting time ad makes code clearer and easier to understand.







