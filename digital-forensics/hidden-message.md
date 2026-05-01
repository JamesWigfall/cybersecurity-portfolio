# Digital Forensics Analysis: Hidden Message Extraction

**Prepared by:** James Wigfall  

---

## Overview

This project demonstrates a basic digital forensics analysis in which a hidden message was extracted from a JPEG file. The objective was to identify, decode, and interpret hidden data using file manipulation and encoding techniques.

---

## Objective

- Identify hidden data within a file  
- Extract and convert the data into a readable format  
- Document the tools and methods used during the analysis  

---

## Methodology

### File Acquisition

The JPEG file (`assignment2.jpg`) was downloaded and initially tested using standard applications:

- Web browser  
- Microsoft Word  
- Adobe Reader  
- macOS Preview  

These methods did not reveal any visible hidden content.

---

### File Manipulation

To further investigate, the file extension was modified:

```bash
assignment2.jpg → assignment2.txt
