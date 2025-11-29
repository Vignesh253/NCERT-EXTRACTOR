////Textbook Metadata Extractor
//Purpose
This tool automatically extracts metadata from NCERT textbook PDF files. It identifies chapter titles, page ranges, subject information, and other details from multiple PDF files at once, saving time compared to manual data entry.

//What It Does
The program analyzes NCERT chapter PDFs and extracts the following information:

Filename

Board (CBSE/NCERT)

Class (1-12)

Subject (Physics, Chemistry, Mathematics, English, etc.)

Medium (English, Hindi, Urdu)

Chapter number

Chapter title

Page range (start page to end page)

Total number of pages

Extraction method used

///Input Format
The tool accepts two types of input:

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
