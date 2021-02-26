---
title: CSS Forms
date: "2021-02-25T22:12:03.284Z"
---

Forms can be created using html, but they usually look really basic and ugly. This is where css comes to play. Css can be used to greatly improve the design and interactiveness of forms. You can add colors, designs , pictures and what ever design you choose to make your forms pleasing to the eye. Lets just say painting an uncompleted building.

For better understanding of the concepts employed in this article, it is required that all readers have a basic knowledge of css properties and a good understanding of html syntaxes.

We will take an example of a simple form i created for this article;
Below you would find a basic HTML form for a “mommy magazine” subscription with no styling, just Html and the same form styled with css. 



>image here


Now lets look at how i achieved this;

Important links used for this project;
In every project you always have to add your link to your css folder to the `<head></head>` tag of your html file. This links all styling done on your css file to your html file. NB This is for those who use external styling alone. 
I also used an external emoji style sheet where i imported the baby emoji for the header of my project. Anything external must be linked in your html header of your project.

>image here


<b>Styling the Form div</b>

In this project i created a div where the form lies in. the background-color property used is to give the form a background color. It could also be an image or pattern  if you choose to bt for this project i chose to use a soiid color. The border-radius property curves the edsges of the form and it can be set to any radius depending on how curved you want it to be. The padding property used centers the form in the middle of the div so it looks well put together and it doesnt spill out. lastly, the width property is used to set the width of the div.


>image here


The border-radius property curves the edsges of the form and it can be set to any radius depending on how curved you want it to be. The padding property used centers the form in the middle of the div so it looks well put together and it doesnt spill out. Lastly, the width property is used to set the width of the div.


<b>Styling the h2 Element</b>
The h2 tag here was used for the tittle of the form being the mommy mag, and this can also be styled in css, you can change the font family, weight and behaviour. The h1 to h6 tags are a static in size so you can choose which size you would prefer to use for your project from 1 being the biggest to 6 being the smallest. 

>image here


Here we only used the font-family to change the font of the heading and the margin-left property to position it in the center of the form. Margins are easy to play with, you can give margins, left, right, top or bottom depending on how you want to move your text or object.



<b>Styling the form Label </b>

Labels are like mini tittles that can be giving to a `<button>`, `<input>`, `<meter>`, `<output>`, `<progress>`, `<select>`, or `<textarea>` element.

>image here


Here, we only change the font-family of the label to make it look more user friendly instead of basic.



<b>Styling the form Textbox </b>
>image here


Here we’ve set a fixed width on the form to prevent it stretching too wide, and set a nice colour and background colour.  Finally we’ve set a pretty grey border around the form, set the border to solid, increased the border radius, used the marginand padding property to arrange them to look neatly and used the boxsizing property to set the type of of box the inout box takes.

<b>Styling the Form Button</b>

>image here


Finally we style our input type “submit” so the the form control buttons are aligned right, and adjust the top, left and right margins so that the subscribe button is nicely placed vertically in the form. Then we style the button itself with a fixed width, a purple background and a border-radius of 4px with no visible border. The font color is also set to white and is padding to appear in the center of the button.

So lets take a look at the end result again,

>image here




