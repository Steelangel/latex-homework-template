latex-homework-template
=======================

LaTeX .sty version of Josh Davis's excellent homework style file. There are a few (major) differences between this file and the original, mostly in macros.  

## Features/How-To
Download the mathhomework.sty file to your working directory. 

The preamble of your document should include the following code to format the title page: 

```
\documentclass{article}
\usepackage{mathhomework}

\hmwkAuthor{Jane L.\ Jankowski} 		% Put your name here
\hmwkNumber{1} 					% What Homework number is this? 
\hmwkDueDate{September 4, 2016} 	% When is this due?
\hmwkClass{My Class}			% Put the name of the Class here!
```

Each homework problem should be put into the `homeworkProblem` environment (note the spelling!)



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
