---
layout: post
title:  "Table Extraction from PDF"
date:   2017-02-09 11:35:04
categories: cv pdf
tags: data-extraction pdf table-extraction
excerpt:  Just some links
---

Example training dataset for table extraction: http://www.tamirhassan.com/dataset.html

Some tools etc.: 

1. Zanran (http://zanran.com/): It claims using computer vision to identify graphs and tables from PDF documents.

See the below example: 
ExampleTableExtraction1.pdf attached: https://s3.amazonaws.com/pdf_demo/ExampleTableExtraction1/ExampleTableExtraction1_images_charts.html

You can clearly notice the inaccurate extraction of the data (from pdf tables) in the .xls files.

2. Tabula (http://tabula.technology/ & git https://github.com/tabulapdf/tabula):  
See how it works at https://source.opennews.org/en-US/articles/introducing-tabula/

3. PDF Tables (https://pdftables.com/): Says using an algorithm which examines the structure in the PDF, and it understands the spacing between items to identify the rows and columns. 


All the above works on text pdf documents, and not on scanned pdfs. So, for now, do not need to worry about the scanned pdfs as most of the pdfs are generally created from applications these days. 

These tools primarily use x, y coordinates of the characters to recognize tables, and then heuristics and computer vision techniques to detect the line boundaries. 

However, all above tools make serious mistakes in extraction, and any of the above would not work well on the attached pdf or similar. 


You can find more websites/tools/libs/research articles by googling pdf table extraction or related.

Some of the useful links which I found earlier in this context:

a) Libs/tools: https://github.com/ashima/pdf-table-extract, http://pdftoxml.sourceforge.net/,  http://www.pdftron.com/pdfgenie/, https://github.com/okfn/pdftables, https://github.com/liberit/scraptils/blob/master/scraptils/tools/pdf2csv.py, 

b) Some Reads: https://schoolofdata.org/2013/06/18/get-started-with-scraping-extracting-simple-tables-from-pdf-documents/, http://craiget.com/blog/extracting-table-data-from-pdfs-with-ocr/, https://scraperwiki.com/2013/07/pdftables-a-python-library-for-getting-tables-out-of-pdf-files/, https://pdfliberation.wordpress.com/

c) OCR: some table extraction tools might require using OCR first. Sample OCR tools on Ubuntu https://help.ubuntu.com/community/OCR,
Cuneiform: https://launchpad.net/cuneiform-linux,
Abbyy (https://www.abbyy.com/en-gb/): de facto OCR company/tool 
