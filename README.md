# Raised Mathematics Project

An open-source project aiming to produce Braille versions of college-level mathematics texts automatically from the source files.

## Results
 Here is a [Braille version of Abstract Algebra: Theory and Applications](results), by Tom Judson.




## Approach

The original source files are written in [PreTeXt](https://pretextbook.org/) -- a mark-up language that uses LaTeX for mathematical expressions and XML mark-up for document structure. The source files can then be compiled, via automated processes, to produce
* HTML version of the book to be read on the web (this version has good accessibility features and can be read by a screen reader, including mathematics expressions);
* PDF file, in case a printed version is needed;
* EPUB version of the book;
* Braille version.

The process to produce Braille is automated. We are using [Speech Rule Engine](https://speechruleengine.org/) to transcribe mathematics (SRE provides Braille output in addition to screen reading). For literary text and overall document formatting (table of contents, etc.), we are using [liblouis](http://liblouis.org/). The results are not yet perfect, but, by estimate of one Braille transcriber, do at least 90% of the transcription work. The work to develop the ability to automatically transcribe the source files was supported by the [American Action Fund for Blind Children and Adults](https://www.actionfund.org/).

The diagrams in the textbook source are created using TiKZ package of LaTeX. A series of scripts enlarges these images as much as possible to fit on a Braille page and transcribes the labels into Braille. The files can then be embossed on an embosser capable of using PDF files. We tested the process on View Plus embossers. The diagrams are embossed separately and then inserted into the embossed textbook. For every diagram, the BRF files have a "throw-away" page with an embossed instruction to replace it by the needed diagram.

## Partners

## Sponsors

