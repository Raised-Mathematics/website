# Raised Mathematics Project

An open-source project aiming to produce Braille versions of college-level mathematics texts automatically from the source files.

## About
This project brings together a group of educators, textbook authors, blind scientists, accessibility specialists and advocates, and companies serving the needs of blind people. Our common goal is to make mathematical texts readily accessible to blind students. Unfortunately, this is not a solved problem, more than 30 years after the Americans with Disabilities Act became the law.

## Challenges
Here is what we believe is wrong with the current status quo.
* Mathematical texts are transcribed to Braille using largely manual process. In many schools, students who need Braille mathematics texts are asked to request the materials at least 6 months ahead of the beginning of the course.
* Due to high cost of Braille production, blind students are often asked to use a screen reader even for complicated mathematical texts.
* Nationwide, there are relatively few specialists who are able to transcribe mathematics materials to and from Braille. Universities who do not have such specialists on staff are not able to provide students with on-demand reliably made Braille copies of course materials.
* We see no clear way to address the flaws in the existing automated processes that take LaTeX files and produce Braille. 

## Approach
We share the approach with [the PreTeXt project](https://pretextbook.org/): it should be possible to compile a single source file for the document into a variety of formats: 
* HTML version with good screen reading;
* PDF file produced with LaTeX;
* EPUB version;
* Braille version.
The structure of the source file should have sufficient semantic information to provide everything that is needed to produce an accessible version of the document.

The goal of Raised Mathematics project is to understand what information is needed in the source file to produce a complete tactile copy of the document and to build and improve the capacity of the compiler that produces Braille.


## Results
 Here is a [Braille version of Abstract Algebra: Theory and Applications](results), by Tom Judson.

The original source files are written in [PreTeXt](https://pretextbook.org/) -- a mark-up language that uses LaTeX for mathematical expressions and XML mark-up for document structure. 

The process to produce Braille is automated. We are using [Speech Rule Engine](https://speechruleengine.org/) to transcribe mathematics (SRE provides Braille output in addition to screen reading). For literary text and overall document formatting (table of contents, etc.), we are using [liblouis](http://liblouis.org/). The results are not yet perfect, but, by estimate of one Braille transcriber, do at least 90% of the transcription work. 

The diagrams in the textbook source are created using TiKZ package of LaTeX. A series of scripts enlarges these images as much as possible to fit on a Braille page and transcribes the labels into Braille. The files can then be embossed on an embosser capable of using PDF files. We tested the process on View Plus embossers. The diagrams are embossed separately and then inserted into the embossed textbook. For every diagram, the BRF files have a "throw-away" page with an embossed instruction to replace it by the needed diagram.

## Partners

* [PreTeXt project](https://pretextbook.org/)
* MathJax
* [Speech Rule Engine](https://speechruleengine.org/)
* View Plus
* American Institute of Mathematics (?)


## Sponsors

The work to develop the ability to automatically transcribe the source files was supported by the [American Action Fund for Blind Children and Adults](https://www.actionfund.org/).


