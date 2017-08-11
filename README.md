latex-homework-template
=======================

LaTeX .sty version of Josh Davis's excellent homework style file. There are a few (major) differences between this file and the original, mostly in macros.  

## Features/How-To
Download the `mathhomework.sty` file to your working directory. Check out the sample file as well. 

The preamble of your document should include the following code to format the title page: 

```
\documentclass{article}
\usepackage{mathhomework}

\hmwkAuthor{Jane L.\ Jankowski}     % Put your name here
\hmwkNumber{1}                      % What Homework number is this? 
\hmwkDueDate{September 4, 2016}     % When is this due?
\hmwkClass{My Class}                % Put the name of the Class here!
```

Each homework problem should be put into the `homeworkProblem` environment (note the spelling!)

Although LaTeX does a good job breaking pages where it is appropriate, you can use `\pagebreak` to force a pagebreak at any point. It's a good idea to use `\pagebreak` between individual homrwork problems for clarity. 

If there is a bonus problem, you can use the `lasthomeworkProblem` environment to mark the last problem, and then use the `bonusProblem` environment to typeset the bonus problem. 

Use `\solution` to mark the solution of the problem. If there are multiple parts to the solution, you can use `\part[]`. The optional input will replace **Part A** with whatever text is inside the brackets. For example: `\part[Hard Part]` will typeset as **Hard Part**. 

### Useful Macros for Mathematics
All of the following are usable in math mode only. 

|Command|Description|
|----|----|
|`\erf`| Error Function|
|`\erfc`| Complimentary Error Function|
|`\mat{}`| Sans-serif matrix notation|
|`\begin{amatrix}` ... `\end{amtrix}`| For augmented matrices| 
|`\ihat`, `\jhat`, `\khat`| _i, j, k_ notation for Vectors|
|`\vec{}`| Boldface vector notation|
|`\div{\vec{}}`| Divergence|
|`\curl{\vec{}}`| Curl|
|`\grad{\vec{}}`| Gradient|
|`\deriv[]{}{}`| The derivative operator. The optional input is the order of the derivative. The second input is the function (this may be left blank), and third is the variable. For example: `\deriv[2]{y}{x}` gives the second derivative of _y_ with respect to _x_, and `\deriv{}{x}` gives the derivative operator with respect to x alone. |
|`dderiv[]{}{}`| Derivative operator in `displaystyle`|
|`pderiv[]{}{}`| Partial derivative operator|
|`dpderiv[]{}{}`| Partial derivative operator in `displaystyle`|
|`\dint`|Larger integral sign|
|`\dx`|Infinitesimal operator: d<em>x</em> as opposed to _dx_. Use for integrals.| 
|`\d`| Infinitesimal operator for non-_x_ variables. Usage: `\,\d y` gives d<em>y</em>|
|`\dot{}`, `\ddot{}` | Overdot(s) for time derivatives|

### Code Listings

For code, use the `listing` environment. The default is set to Python code style. 

## Installing

1. First you'll need LaTeX. Instructions on obtaining it can be found here:
   http://latex-project.org/ftp.html
2. Compiling from the command line will look like the following:

   ```bash
   $ latexmk homework.tex
   ```
3. Or you can use [TeXShop][texshop] or a similar native client to typeset the
   LaTeX file.

## Credit

All credit for the initial design goes to [Josh Davis][josh]. Thanks!

## License

This code is distributed under the MIT license. For more info, read the
[LICENSE](/LICENSE) file distributed with the source code.

[texshop]: http://pages.uoregon.edu/koch/texshop/
[josh]: https://github.com/jdavis
