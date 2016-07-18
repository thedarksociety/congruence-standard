[![Open Source Love](https://badges.frapsoft.com/os/gpl/gpl.svg?v=102)](https://github.com/ellerbrock/open-source-badge/)
Congruence, for CSS
===================
A collection of design principles and language patterns for writing cohesive, scalable CSS.

### Table of Contents ###

1. [Introduction](#introduction)
2. [Organization](#organization)
    * [Spacing](#spacing)
    * [Property Declaration](#property-declaration-order)
    
Introduction
------------
>
> Without good design, whats the point?
>

This guide is meant to promote a consistent and successive philosophy around keeping code clean, intentional, and 
maintainable. Each approach may have it's strengths and weaknesses; however, this document doesn't focus on 
providing perfect solutions, but rather, solutions that combine the best balance of value for time.

Although currently incomplete, this is a community driven document. New ideas are always welcome. Please contribute.

Organization
--------------------------

### Whitespace
Improves the readability of the codebase and mood of the developers when kept consistent.
 
 * Either choose soft indents or real tabs for indentation
 * Use four spaces per indentation level
 * Never mix tabs and spaces
 * Space before opening brace `{` of rule declarations
 * Space after `:` in rule property 
 * Closing brace `}` of declaration put on new line
 * Empty line between rule declarations
 * Multiple selectors in a declaration must be put on a new line

### Property Declaration Order
Yet another opinionated way for declaring the order of CSS properties.

 * [Content](#content)
 * [Positioning](#positioning)
 * [Setup](#setup)
 * [Table](#table)
 * [Box Model](#box-model)
 * [Background](#background)
 * [Typography](#typography)
 * [Type Layout](#type-layout)
 * [Misc](#misc)
 * [Animation](#animation)

#### Content ####
```css

.selector {

    /**
     * NOTE: Does the quotes property need to come
     *       at the beginning since content will
     *       place them there as a value anyway?
     *
     * TODO Research usage of quotes placement
     */
    content: normal;
    quotes: '\201C' '\201D' '\2018' '\2019';
}

````

#### Positioning ####
```css

.selector {
    position: static;
    z-index: auto;
    top: auto;
    bottom: auto;
    left: auto;
    right: auto;
    float: none;
    clear: none;
    
    /** 
     * NOTE: flex property is also included in this
     *       section and follows the property for a
     *       `left` positioning value.
     */
    flex-direction: row;
    flex-wrap: nowrap;
    flex-flow: row nowrap;
    justify-content: flex-start;
    align-items: stretch;
    align-content: stretch;
    order: 0;
    flex: 0 1 auto;
    flex-grow: 0;
    flex-shrink: 1;
    flex-basis: auto;
    align-self: auto;
}

````

#### Setup ####
```css

.selector {
    display: inline;
    visibility: visible;
    opacity: 1;
    overflow: visible;
    overflow-x: visible;
    overflow-y: visible;
    clip: auto;
}

````

#### Table ####
```css

.selector {
    caption-side: top;
    table-layout: auto;
    empty-cells: show;
}

````

#### Box Model ####
```css

.selector {
    margin: 0;
    margin-bottom: 0;
    margin-left: 0;
    margin-right: 0;
    margin-top: 0;
    outline: none;
    outline-width: medium;
    outline-style: dotted;
    outline-color: #C0C0C0;
    outline-offset: 100px;
    border: 0;
    border-style: none;
    border-width: medium;
    border-color: inherit;
    border-collapse: separate;
    border-image: none;
    border-spacing: 0;
    border-bottom: 0;
    border-bottom-color: inherit;
    border-bottom-style: none;
    border-bottom-width: medium;
    border-left: 0;
    border-left-color: inherit;
    border-left-style: none;
    border-left-width: medium;
    border-right: 0;
    border-right-color: inherit;
    border-right-style: none;
    border-right-width: medium;
    border-top: 0;
    border-top-color: inherit;
    border-top-style: none;
    border-top-width: medium;
    border-radius: 0;
    border-top-left-radius: 0;
    border-top-right-radius: 0;
    border-bottom-left-radius: 0;
    border-bottom-right-radius: 0;
    box-shadow: none;
    box-sizing: content-box;
    width: auto;
    min-width: 0;
    max-width: none;
    height: auto;
    min-height: 0;
    max-height: none;
    padding: 0;
    padding-top: 0;
    padding-right: 0;
    padding-bottom: 0;
    padding-left: 0;
}

````

#### Background ####
```css

.selector {
    background : 0;
    background-color : transparent;
    background-image: -webkit-linear-gradient(top, #000, #fff);
    background-image:    -moz-linear-gradient(top, #000, #fff);
    background-image:     -ms-linear-gradient(top, #000, #fff);
    background-image:      -o-linear-gradient(top, #000, #fff);
    background-image:         linear-gradient(top, #000, #fff);
    background-repeat : repeat;
    background-position : 0 0;
    background-position-x : 0;
    background-position-y : 0;
    background-size : auto auto;
    background-origin : padding-box;
    background-attachment : scroll;
    background-clip : border-box;
}

````

#### Typography ####
```css

.selector {
    font-size: 100%;
    font-size-adjust: none;
    line-height: normal;
    font-family: sans-serif;
    -moz-osx-font-smoothing: inherit;
     -webkit-font-smoothing: none;
    font-style: normal;
    font-weight: normal;
    font-variant: normal;
    font-stretch: normal;
    hyphens: none;
    word-spacing: inherit;
    letter-spacing: 1px;
    color: #212121;
}

````

#### Type Layout ####
```css

.selector {
    direction: ltr;
    text-align: center;
    text-decoration: none;
    text-indent: each-line;
    text-overflow: clip;
    text-rendering: auto;
    text-shadow : none;
    text-transform: none;
    word-break: normal;
    word-wrap: normal;
    white-space: inherit;
    vertical-align: baseline;
    list-style: none;
    list-style-type: disc;
    list-style-position: outside;
    list-style-image: none;
}

````

#### Misc ####
```css

.selector {
    pointer-events: auto;
    cursor: pointer;
    filter: inherit;
    size: 0;
    zoom: normal;
    resize: none;
    -webkit-appearance: inherit;
       -moz-appearance: inherit;
    -webkit-user-select: inherit;
       -moz-user-select: inherit;
        -ms-user-select: inherit;
    -ms-interpolation-mode: inherit;
    marks: none;
    page-break-after : auto;
    page-break-before : auto;
    page-break-inside : auto;
    unicode-bidi : normal;
}

````

#### Animation ####
```css

.selector {
    backface-visibility: visible;
    perspective: none;
    perspective-origin: 50% 50%;
    -webkit-transform: rotate(45deg);
       -moz-transform: rotate(45deg);
        -ms-transform: rotate(45deg);
         -o-transform: rotate(45deg);
            transform: rotate(45deg);
    transform-origin: 50% 50% 0;
    transform-style: flat;
    animation: none;
    animation-delay: 0;
    animation-direction: normal;
    animation-duration: 0;
    animation-fill-mode: none;
    animation-iteration-count: 1;
    animation-name: none;
    animation-play-state: running;
    animation-timing-function: ease;
    -webkit-transition: color 0.3s ease;
       -moz-transition: color 0.3s ease;
        -ms-transition: color 0.3s ease;
         -o-transition: color 0.3s ease;
            transition: color 0.3s ease;
    transition-delay: 0s;
    transition-duration: 0s;
    transition-property: none;
    transition-timing-function: ease;
}

````