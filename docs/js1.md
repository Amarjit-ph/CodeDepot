---
id: js1
title: Javascript
sidebar_label: Introduction
---

## Introduction

JavaScript is a dynamic, weakly typed programming language, Which is compiled at runtime, It can be executed as a part of webpage in a browser or directly on any machine.

Created at 1995 by Brendan Eich While he was an engineer at Netscape.

Created to make webpages more dynamic originally called LiveScript but due to popularity of Java It is called JavaScript.

- Dynamic weakly typed programming language
- Interpreted on the fly
- Hosted language Runs in different environments
- Most prominent use : Run code in a browser

## Dynamic & Weakly typed

Not pre-compiled instead parsed and Compile Fast (In browser), Code evaluated and executed in runtime, Code can change at runtime.

Data types are assumed automatically, You don't define that some variable has to hold a certain value, Data types can change.

## Javascript Execution

**Javascript Execution**<br/>Your code > JavaScript engine > Effect on webpage

**JavaScript Engine** <br/>Parse Code > Compile to machine code > Execute Machine Code <br/>[ Single Thread ]

- V8 (chrome)
- SpiderMonkey (Firefox)
- Chakra (Edge)

## Host Environment

**Browserside**

1. JavaScript was invented to create more dynamic websites by executing in the browser
2. JavaScript can manipulate the HTML code,CSS, send background Http requests & much more
3. JavaScript CAN’T access the local filesystem, interact with the operating system etc.

**Server Side**

1. Google’s JavaScript Engine (V8) was extracted to run JavaScript anywhere (called “Node.js”)
2. Node.js can be executed on any machine and is therefore often used to build web backends (server-side JavaScript)
3. Node.js CAN access the local filesystem,interact with the operating system etc. It Can't manipulate HTML or CSS

```css title="History of Javascript"
LiveScript - 1995
Microsoft releases its own version for IE

ECMA = European Computer Manufactures Association
A standards organization that evolves the ECMAScript language

Javascript - The most famous ECMAScript implementation
(other Example "ActionScript" or "Jscript")

ECMA - Late 1996
ES1 1997
ES2 1998
ES3 1999
ES4 Abandoned
ES5 2009
ES6 2015
ES7 2016
ES8 2017
ES9 2018
```
