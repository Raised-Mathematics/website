# Raised Mathematics Project

An open-source project aiming to produce Braille versions of college-level mathematics texts automatically from the source files.

## Results
 Here is a Braille version of Abstract Algebra: Theory and Applications, by Tom Judson.

The book, available [on the web](http://abstract.ups.edu/aata/aata.html) and [as a PDF file](http://abstract.pugetsound.edu/download.html), has been converted to Braille, using Nemeth Braille conventions for mathematics. The textbook is an open-source text. All the source files for it can be found on [github](https://github.com/twjudson/aata). 

The Braille version of the textbook is quite long. The most recent PDF file for the textbook has nearly 400 pages, and the Braille version has about 1700 Braille pages. For this reason, we split the text by chapters.

### Textbook, with placeholder pages for diagrams

The BRF files have not been edited at all (only split by chapter).

* [Front matter](brf_files/chunk0.brf)
* [Chapter 1](brf_files/chunk1.brf)
* [Chapter 2](brf_files/chunk2.brf)
* [Chapter 3](brf_files/chunk3.brf)
* [Chapter 4](brf_files/chunk4.brf)
* [Chapter 5](brf_files/chunk5.brf)
* [Chapter 6](brf_files/chunk6.brf)
* [Chapter 7](brf_files/chunk7.brf)
* [Chapter 8](brf_files/chunk8.brf)
* [Chapter 9](brf_files/chunk9.brf)
* [Chapter 10](brf_files/chunk10.brf)
* [Chapter 11](brf_files/chunk11.brf)
* [Chapter 12](brf_files/chunk12.brf)
* [Chapter 13](brf_files/chunk13.brf)
* [Chapter 14](brf_files/chunk14.brf)
* [Chapter 15](brf_files/chunk15.brf)
* [Chapter 16](brf_files/chunk16.brf)
* [Chapter 17](brf_files/chunk17.brf)
* [Chapter 18](brf_files/chunk18.brf)
* [Chapter 19](brf_files/chunk19.brf)
* [Chapter 20](brf_files/chunk20.brf)
* [Chapter 21](brf_files/chunk21.brf)
* [Chapter 22](brf_files/chunk22.brf)
* [Chapter 23 and end matter](brf_files/chunk23.brf)

### Diagrams

The machine-converted diagram for the textbook are in this [ZIP file](diagrams/PicturesAATA.zip). The files names contain the section number and the figure number. Some of the diagrams required editing, edited versions are available.


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

