NCERT Textbook Metadata Extractor
Purpose
This tool automatically extracts metadata from NCERT textbook PDF files. It identifies chapter titles, page ranges, subject information, and other details from multiple PDF files at once, saving time compared to manual data entry.

What It Does
The program analyzes NCERT chapter PDFs and extracts the following information:

Filename

Board (CBSE/NCERT)

Class (1–12)

Subject (Physics, Chemistry, Mathematics, English, etc.)

Medium (English, Hindi, Urdu)

Chapter number

Chapter title

Page range (start page → end page)

Total number of pages

Extraction method used (TOC, Visual, etc.)

Input Format
The tool accepts:

ZIP file containing multiple chapter PDFs

Single PDF file

Output Format
Results are provided in two downloadable formats:

CSV file – can be opened in Excel or Google Sheets

JSON file – suitable for databases or other programs

Both contain the same extracted metadata, just in different formats.

How It Works
Upload a ZIP of NCERT chapter PDFs or a single PDF.

The program automatically:

Identifies board, class, subject, and medium from filenames.

Scans for a Table of Contents (ps.pdf / contents) if available.

Extracts chapter titles from the first page of each PDF.

Detects physical page numbers printed on the pages.

Calculates page ranges using start page and PDF length.

Cleans and standardizes all extracted text.

The extracted data is shown in a table in the interface.

You can download the results as CSV or JSON.

Key Features
Smart Title Extraction
Different strategies are used based on subject:

Science subjects (Physics, Chemistry, Mathematics, Science):
Uses font size and layout analysis to detect the main title.

Language subjects (English, other language books):
Uses heuristic and structure-based analysis to find the correct title block.

Text Cleaning
The tool automatically fixes common OCR and layout issues:

Corrects spaced letters:

E v e l i n e → Eveline

Merges broken words:

U NITS → UNITS

Removes duplicate words or phrases:

Title Title → Title

Filters out headers, footers, and page numbers.

Validation
Cross-checks extracted titles against the Table of Contents when available.

If the physical start page matches an entry in the TOC map, the TOC title overrides the visually extracted title (treated as golden source).

Technical Requirements
Python libraries:

gradio

pandas

PyMuPDF (fitz)

pdfplumber

(Install via pip before running the tool.)

Filename Convention
The tool is optimized for NCERT-style filenames, for example:

lekl101.pdf → Class 12, English, Kaleidoscope, Chapter 1

keph102.pdf → Class 11, Physics, Chapter 2

Chapter numbers are automatically parsed from these codes.

Limitations
Designed specifically for NCERT (and NCERT-like) textbook PDFs.

Works best when filenames follow standard NCERT patterns.

Requires PDFs with embedded text; pure scanned images without OCR may not work well.

Usage
Run the program.

Click “Upload ZIP or PDF”.

Select your NCERT ZIP or PDF file.

Click “Extract Metadata”.

Wait for processing to finish.

Download the CSV or JSON from the provided buttons.
ZIP file containing multiple PDF files

Single PDF file

///Output Format
Results are provided in two formats for download:

CSV file - Can be opened in Excel or Google Sheets

JSON file - For use in databases or programming applications

Both files contain the same extracted metadata in different formats.

////How It Works
Upload a ZIP file containing NCERT chapter PDFs or a single PDF

The program automatically:

Identifies the board, class, and subject from filenames

Scans for a Table of Contents if available

Extracts chapter titles from the first page of each PDF

Detects physical page numbers

Calculates page ranges

Cleans and standardizes all text

View the extracted data in a table on screen

Download the results as CSV or JSON files

////Key Features
Smart Title Extraction
The program uses different methods depending on the subject:

Science subjects (Physics, Chemistry, Math): Uses font size analysis to find titles

Language subjects (English): Uses keyword and structure analysis to find titles

Text Cleaning
Automatically fixes common issues in extracted text:

Corrects spaced letters: "E v e l i n e" becomes "Eveline"

Merges broken words: "U NITS" becomes "UNITS"

Removes duplicate words: "Title Title" becomes "Title"

Removes headers and page numbers

Validation
Cross-references extracted titles with the Table of Contents when available to ensure accuracy.

Technical Requirements
The program requires these Python libraries:

gradio

pandas

PyMuPDF (fitz)

pdfplumber

////Filename Convention
The tool works with NCERT filename patterns such as:

lekl101.pdf (Class 12, English, Kaleidoscope, Chapter 1)

keph102.pdf (Class 11, English, Physics, Chapter 2)

Chapter numbers are automatically parsed from these codes.



/////Usage
Run the program

Click "Upload ZIP or PDF"

Select your file

Click "Extract Metadata"

Wait for processing to complete

Download CSV or JSON file using the download buttons
