---
title: Animating with CSS
date: "2021-02-26T23:46:37.121Z"
---


<b>Introduction</b>

CSS animation is a vast topic once you get in. It allows you to animate HTML elements without javascript and flash. CSS continues to evolve as a language thereby giving us a more exceptional ability to create with code.

An animation executes as soon as the animation property is applied, with CSS animations, there is a bit more control. They allow for the creation of multiple keyframes over which animation occurs.
CSS animations have a lot of great benefits. You can choose how many times the animation should run and which direction it should run. You can also set the animation to be running or paused.

This article starts you on your path to animating with CSS. It shows you how to work with CSS animation in modern browsers, how to use keyframes and how to make changes to animations with CSS properties. Now let's get to it.


<b>What do Animations do?</b>

Animations enable animation of transitions from one CSS style configuration to another. It consists of two segments, a style-defining the CSS animation and a set of keyframes that point out the start and end states of the animation’s style.


<b>Advantages of CSS animations over Script driven animations</b>

CSS animations are used to create simple animations without using javascript. The animations created using CSS run well even under moderate system load. This functionality allows the browser to control the animation sequence, optimizing efficiency and performance.


<b>Why Animate?</b>

The animation is important because it helps improve usability and general user experience. It also draws a users attention to something or directs them through a flow.


<b> Browser Support for CSS Animations </b>

CSS animations work in all modern browsers. A vendor prefix is necessary for animations to work on some browsers.

Internet Explorer 10 and newer, Firefox, Internet Explorer Mobile - no vendor prefix needed.
Safari, Chrome, Opera, iOS Safari, Android browser and Blackberry browser all use the `-webKit` vendor prefix.

In iOS 6.1 and earlier, pseudo-elements do not support animations.
Opera mini and Internet Explorer 9, the fall back is to create the animation using Javascript. You first check to detect CSS animation support then use one of the Javascript libraries.


<b> @Keyframes rule </b>

Keyframes are used to define the sequence of the animation. A series of keyframes defines the behavior for one cycle through the animation.

Keyframe selectors are used to specifying animation. It specifies a percentage of the animation duration. When you specify CSS styles inside the `@keyframes` rule, the animation gradually changes from the current style to the new style at specified times. Each keyframe outlines how the animated element should behave at a given time during the animation sequence.

A keyframes rule starts with the `@keyframes` keyword followed by an identifier which is the keyframe name. Inside the braces are a list of CSS properties and values to set the style for the specific states.

Keyframes use a `<percentage>` to specify the time during the animation sequence at which they take place. 0% specifies the first moment while 100% specifies the last state of the animation. Unique aliases are used to specify: from and to. The keyword from is equivalent to 0% while to is equivalent to 100%.

For an animation to work, the animation must be bound to an element.

`@keyframes` identifier
`@-webkit-keyframes` identifier 
{
list of properties and values
}

Below is a simple example that has been created showing how keyframes work. Unique aliases like from and to are used in this example to show the sequence of the animation from the beginning with a change of color, to the end of the sequence.


    <html>                                                          
    <head>
    <link rel="stylesheet" type="text/css" href="style.css" />
    </head>
    <body>
    <h2>Animation Example</h2>
    <div id="example">
    <div class=”bounce”></div>
    </div>
    </body>
    </html>
    #example
    {
      width: 300px;
      height: 300px; 
    }
    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:orange;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 10s;
      -webkit-animation-duration: 10s;
    }
    @keyframes bounce
    @-webkit-keyframes bounce
     {
      from {background-color: skyblue;}
      to {background-color: orange;}
    }


<b> Animation Properties </b>

To create an animation sequence, you can style the animation with the following animation properties. CSS animation provides 8 essential properties for controlling animations.


<b> Animation-name </b>

The `animation-name` property defines the specific name of the `@keyframes` rule that contains the properties that will be animated.

In the example below, a simple animation named bounce is created. The animation color changes the `background-colour` of the `div` element when the animation is 25% complete, 50% complete, 75% complete and 100% complete.

This example is used to explain some of the properties of css animations in this article.

    <html>                                                           
    <head>
    <link rel="stylesheet" type="text/css" href="style.css" />
    </head>
    <body>
    <h2>Animation Example</h2>
    <div id="example">
    <div class=”bounce”></div>
    </div>
    </body>
    </html>
    #example
    {
        width:300px;
        height: 300px;
    }
    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce;
      -webkit-animation-name: bounce;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }



<b> Animation-duration </b>

The `animation-duration` property defines the amount of time an animation should last during one cycle of the animation.

In the example below, the duration of the animation is set to 5 seconds.


    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }


<b> Animation-iteration-count </b>

The `animation-iteration-count` property states the number of times an animation should run. It can either take a particular value or be set to run infinitely.

In the example below, the animation will run 4 times before it stops.

    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count: 4;
      -webkit-animation-iteration-count: 4;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }


<b> Animation-delay </b>

The `animation-delay` property states when an animation starts from the time the element is loaded and the beginning of the animation.

In the example below, the animation is delayed for 3 seconds before it starts.
 
    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count: 4;
      -webkit-animation-iteration-count: 4;
      animation-delay:3s;
      -webkit-animation-delay: 3s;
    }
    @keyframes bounce
    @-webkit-keyframes bounce 
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }


<b> Animation-direction </b>

The `animation-direction` property states whether an animation runs forward, in reverse or alternate cycles. 
The `animation-direction` property has four values;

<b> normal </b>: This value specifies the animation to be played forwards, as usual.<br>
<b> reverse </b>: This value specifies that the animation is played backward.<br>
<b> alternate </b>: This value causes the animation to alternate between normal and reverse. It moves forward and then backwards.<br>
<b> alternate-reverse </b>: This value causes the animation to alternate between reverse and normal. It moves backward and then forwards.

In the example below, the animation will move in the alternate-reverse direction.

    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count: 4;
      -webkit-animation-iteration-count: 4;
      animation-delay: 3s;
      -webkit-animation-delay: 3s;
      animation-direction: alternate-reverse;
      -webkit-animation-direction: alternate-reverse; 
    }
    @keyframes bounce
    @-webkit-keyframes bounce 
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }


<b> Animation-fill-mode </b>

The `animation-fill-mode` property designates a style for the animation before it starts after it ends or both.
The `animation-fill-mode` property takes the following keyword values;

<b>none</b>: This acts as the default and does not apply and value or styles the animation before or after it is executing.<br>
<b>forwards</b>: applies the property values after the animation stops. If the `animation-iteration-count` value is greater than 0, the values applied are those at the end of the last completed iteration. If the count value equals 0, the values applied are those that start the first iteration.<br>
<b>backwards</b>: applies the property values defined in the first keyframe that starts the first iteration to the period defined by `animation-delay`. The values come from either the 0% (from) or 100% (to) keyframes, depend- ing on the value of the `animation-direction` property.<br>
<b>both</b>: This does what you might expect and applies both the forwards and backward values to the `animation-fill-mode` property.

In the example below, the animation fill mode property is set to forwards.


    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count:4;
      -webkit-animation-iteration-count: 4;
      animation-delay:3s;
      -webkit-animation-delay: 3s;
      animation-direction: alternate-reverse;
      -webkit-animation-direction: alternate-reverse; 
      animation-fill-mode: forwards;
      -webkit-animation-fill-mode: forwards;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }



<b> Animation-play state </b>

Typically, animations run as soon as the `animation-name` property is assigned. However, that can be changed using the `animation-play-state` property. This property specifies if an animation is running or paused.
The default value for animation is running. If the value changes to paused, the animation stops where it is until the `animation-play-state` changes to running. When paused, the animation displays whatever state the animation was in at that moment. When the animation is resumed, it restarts from the state it was paused in.

In the example below, the animation play state is set to either paused or running.


    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce; 
      -webkit-animation-name: bounce;
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count:4;
      -webkit-animation-iteration-count: 4;
      animation-delay:3s;
      -webkit-animation-delay: 3s;
      animation-direction: alternate-reverse;
      -webkit-animation-direction: alternate-reverse; 
      animation-play-state: paused;
      -webkit-animation-play-state: paused;
      animation-play-state: running;
      -webkit-animation-play-state: running;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }



<b> Animation-timing-function </b>

The `animation-timing-function` property arranges the timing of the animation by designating a speed curve for each keyframe in an animation cycle.
The `animation-timing-function` property has the following values;

- ease
- linear
- ease-in
- ease-out
- ease-in-out
- cubic-bezier
- step-start
- step-end
- steps()

In the example below, shows four different speed curves that can be used. 


    #example
    {
        width:300px;
        height: 300px;
    }
    .bounce .bounce2 .bounce3 .bounce4
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation-name: bounce;
      -webkit-animation-name: bounce; 
      animation-duration: 5s;
      -webkit-animation-duration: 5s;
      animation-iteration-count:4;
      -webkit-animation-iteration-count: 4;
      animation-delay: 3s;
      -webkit-animation-delay: 3s;
    }
    .bounce
    {
      animation-timing-function: linear;
      -webkit-animation-timing-function: linear;
    }
    .bounce2
    {
      animation-timing-function: ease;
      -webkit-animation-timing-function: ease;
    }
    .bounce3
    {
      animation-timing-function: ease-in;
      -webkit-animation-timing-function: ease-in;
    }
    .bounce4
    {
      animation-timing-function: ease-in-out;
      -webkit-animation-timing-function: ease-in-out;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        from{background-color: skyblue; left:0px; top:0px;}
        to{background-color: purple; left:200px; top:0px;} 
    }



<b> Animation-shorthand </b>

For simplicity, rather than listing all the animation properties, the same animation effect can be achieved by using a shorthand property as shown below.


    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation: bounce 5s infinite 3s alternate-reverse paused; 
      -webkit-animation: bounce 5s infinite 3s alternate-reverse paused;
    }
    @keyframes bounce 
    @-webkit-keyframes bounce
    {
        0%{background-color: skyblue; left:0px; top:0px;}
        25%{background-color: purple; left:200px; top:0px;}
        50%{background-color: orange; left:200px; top:200px;}
        75%{background-color: hotpink; left:0px; top:200px;}
        100%{background-color: green; left:0px; top:0px;} 
    }

I have created another simple animation with more sequences that you can play around with.
 

    .bounce
    {
      width: 50px;
      height: 50px;
      border-radius: 20px;
      position: relative;
      background-color:skyblue;
      animation: bounce 5s infinite 3s alternate-reverse paused; 
      -webkit-animation: bounce 5s infinite 3s alternate-reverse paused;
    }
    @keyframes bounce
    @-webkit-keyframes bounce
     {
    0% {background-color: skyblue; left:0px; top:0px;}
    10% {background-color: purple; left:100px; top:200px;}
    20% {background-color: orange; left:200px; top:0px;}
    30% {background-color: hotpink; left:300px; top:200px;}
    40% {background-color: green; left:400px; top:0px;}
    50% {background-color: orangered; left:500px; top:200px;}
    60% {background-color: red; left:400px; top:0px;}
    70% {background-color: blue; left:300px; top:200px;}
    80% {background-color: indigo; left:200px; top:0px;}
    90% {background-color: brown; left:100px; top:200px;}
    100% {background-color: orchid; left:0px; top:0px;}
    }




<b> Summary </b>

As we can see, CSS is becoming a more powerful language in the world of front end development. It is now not only used in styling, but creating animations, and in time, more CSS properties will be created to make animations quicker. 
In this article, we have learnt about the 8 properties of CSS animations which are the name, delay, direction, iteration-count, fill-mode, play- state, timing-function and shorthand. We also talked about browsers that support CSS animations and its advantages over script driven and the use of keyframes, and how they define the behaviour of an animation.
These above tools are used to create simple animations that do not need Java script and are modern browser friendly. CSS animations allow for smooth animation changes of one or multiple CSS properties.

