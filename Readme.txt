Discharge Summary Agent

Overview

This project extracts clinical information from scanned patient documents and generates a structured
discharge summary.
The workflow includes:

PDF to Image Conversion
OCR Text Extraction using Tesseract
Clinical Information Extraction
Missing Information Detection
Discharge Summary Generation
JSON Output Generation

Requirements

Install the required Python packages:

pip install pytesseract
pip install pillow
pip install pymupdf

Install Tesseract OCR:

Windows:

Download Tesseract OCR
Install it
Verify installation:
tesseract --version

Workflow

Step 1: Convert PDF to Images
The scanned PDF is converted into PNG images.
Example:
patient.pdf
 ↓
page_0.png
page_1.png
...
page_70.png
Step 2: OCR Processing
Each image is processed using Tesseract OCR.

Example:
text = pytesseract.image_to_string(image)

Step 3: Clinical Information Extraction

The system extracts:

Diagnoses
Symptoms
Laboratory Findings
Medications
Pending Results
Follow-up Information
Step 4: Missing Information Detection
The system identifies unavailable fields such as:
Patient Name
Age
Gender
Discharge Date

Step 5: Generate Structured Summary

Step 6: Generate Discharge Summary

Features

OCR-based document processing
Clinical information extraction
Missing information detection
Structured JSON output
Human-readable discharge summary
Agent execution trace

Limitations

OCR quality depends on scan quality.
Handwritten notes may not be extracted accurately.
Some patient information may require manual review.

Future Improvements

Automatic medication reconciliation
Conflict detection across notes
LLM-based diagnosis extraction
Advanced clinical entity recognition
Multi-document summarization


