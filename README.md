
# AI DDR Report Generator

## Overview
This project demonstrates an **AI-assisted workflow that automatically converts technical inspection documents into a structured, client-ready Detailed Diagnostic Report (DDR).**

The system processes two types of reports:

- **Inspection Report** – Contains site observations and issues.
- **Thermal Report** – Contains thermal images and temperature readings.

The system extracts information from both documents, merges the findings, and produces a **fully structured diagnostic report in Word format**.

---

# Problem Statement
Technical inspection data is usually distributed across multiple documents containing text, images, and temperature measurements.  

Manually converting these into a **clear diagnostic report** is time-consuming and prone to errors.

This project automates the process by:

- Extracting observations from inspection reports
- Extracting thermal hotspot and coldspot data
- Matching temperature anomalies with room observations
- Generating a **structured client-ready DDR report automatically**

---

# Key Features

## Automatic Document Processing
The system reads both:

- Inspection PDF
- Thermal Report PDF

and extracts the relevant observations automatically.

## Image Extraction
Images are extracted directly from the source reports and placed under the appropriate sections in the final report.

## Thermal Data Mapping
Thermal hotspot and coldspot temperatures are detected and linked to the corresponding rooms or areas.

## Structured DDR Generation
The final report follows the required **7-section DDR format**:

1. Property Issue Summary  
2. Area-wise Observations  
3. Probable Root Cause  
4. Severity Assessment  
5. Recommended Actions  
6. Additional Notes  
7. Missing or Unclear Information  

## Handling Imperfect Data
The system is designed to:

- Avoid duplicate findings
- Detect missing data
- Explicitly mention **"Not Available"** when information is missing
- Flag conflicting information between reports

## Generalizable System
The workflow is designed to **work on similar inspection + thermal reports**, not only the provided sample documents.

---

# System Workflow

```
Input Reports
     │
     ▼
PDF Processing
(Text + Image Extraction)
     │
     ▼
Thermal Data Detection
(Hotspots / Coldspots)
     │
     ▼
Room Mapping
(Thermal + Inspection Observations)
     │
     ▼
Information Structuring
     │
     ▼
DDR Report Generation
(.docx Output)
```

---

# Output

The system generates a **client-ready Detailed Diagnostic Report (DDR)** in **Microsoft Word (.docx)** format.

Example report structure:

```
Detailed Diagnostic Report

1. Property Issue Summary
2. Area-wise Observations
3. Probable Root Cause
4. Severity Assessment
5. Recommended Actions
6. Additional Notes
7. Missing or Unclear Information
```

Relevant images from the reports are placed under their corresponding observations.

---

# Technologies Used

- **Python**
- PDF processing libraries for **text and image extraction**
- Basic **NLP techniques** for structuring observations
- Automated **Word document generation (.docx)**

---

# Limitations

Thermal image-to-room matching currently relies on **text references inside the reports** rather than computer vision.

Since **no paid APIs or vision models were used**, the system does not perform visual thermal anomaly detection directly from images.

---

# Future Improvements

Potential upgrades for a production-ready system:

- Computer Vision models for **thermal anomaly detection**
- AI-based **room classification**
- Automated **severity scoring using machine learning**
- Web interface for **uploading reports**
- Support for **multiple inspection report formats**
- Integration with **LLM-based reasoning systems**

---

# Example Use Case

Input:
- Inspection Report PDF
- Thermal Report PDF

Output:
- Fully structured **Detailed Diagnostic Report (DDR)** ready for client delivery.

---

# Author

**Aditya Chavan**  

AI / Machine Learning Enthusiast  
Focused on building **practical AI systems, automation pipelines, and intelligent workflows**.
