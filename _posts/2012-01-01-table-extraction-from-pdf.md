---
layout: post
title:  "Table Extraction from PDF"
date:   2017-02-09 11:35:04
categories: cv pdf
tags: data-extraction pdf table-extraction
excerpt:  Just some links
---

1. [Example training dataset for table extraction](http://www.tamirhassan.com/dataset.html)

2. [Zanran: provides table extraction](http://zanran.com/): It claims using computer vision to identify graphs and tables from PDF documents.

   [Example Table Extraction from PDF using Zanran](https://s3.amazonaws.com/pdf_demo/ExampleTableExtraction1/ExampleTableExtraction1_images_charts.html)
   
   [Download PDF Sample here](https://github.com/kasooja/kasooja.github.io/tree/master/resources/ExampleTableExtraction1.pdf)

You can easily notice many inconsistencies in data extraction from pdf tables in the .xls files.

3. [Tabula: provides table extraction and freely available](http://tabula.technology/) 

   [Git repo](https://github.com/tabulapdf/tabula) 
    
   [See how it works here](https://source.opennews.org/en-US/articles/introducing-tabula/)

4. [PDF Tables: provides table extraction](https://pdftables.com/): Uses an algorithm which examines the structure in the PDF, and it understands the spacing between items to identify the rows and columns. 


All the above works on text pdf documents, and not on scanned pdfs. 
However, most of the current pdfs are generally exported/created from applications these days. 

These tools primarily use x, y coordinates of the characters to recognize tables, and then heuristics and computer vision techniques to detect the line boundaries. 

However, all above tools are not perfect, and make some serious mistakes in extraction, and any of the above would not work well on the pdf provided in the second example.

You can find more websites/tools/libs/research articles by searching pdf table extraction or related.

Some of the useful links which I found earlier in this context:

a) Libs/tools: [1](https://github.com/ashima/pdf-table-extract), [2](http://pdftoxml.sourceforge.net/), [3](http://www.pdftron.com/pdfgenie/), [4](https://github.com/okfn/pdftables), [5](https://github.com/liberit/scraptils/blob/master/scraptils/tools/pdf2csv.py) 

b) Some Reads: [1](https://schoolofdata.org/2013/06/18/get-started-with-scraping-extracting-simple-tables-from-pdf-documents/), [2](http://craiget.com/blog/extracting-table-data-from-pdfs-with-ocr/), [3](https://scraperwiki.com/2013/07/pdftables-a-python-library-for-getting-tables-out-of-pdf-files/), [4](https://pdfliberation.wordpress.com/)

c) OCR: some table extraction tools might require using OCR first.

   [Sample OCR tools on Ubuntu](https://help.ubuntu.com/community/OCR)
    
   [Cuneiform](https://launchpad.net/cuneiform-linux)
   
   [Abbyy](https://www.abbyy.com/en-gb/): A popular OCR company. 
