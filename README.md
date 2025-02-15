# Optical Character Recognition (OCR) for Patient Medical Forms
#Note : Please Go through the comment on the code file being given for easy understanding
## 📌 Description
This project focuses on Optical Character Recognition (OCR) to extract specific patient details from medical forms and store them in a database. The research involved an in-depth comparison of two OCR technologies: **pytesseract** and **EasyOCR** to determine their efficiency in extracting text from images.

## 🚀 Technologies Used
- **Python Libraries**: OpenCV, NumPy, Pillow
- **OCR Technologies**: pytesseract, EasyOCR
- **Image Processing Techniques**: Grayscale, Thresholding, Dilation, Resolution Enhancement, Morphological Operations
- **Database**: MySQL
- **Python-SQL Connectivity**: MySQL Connector

## ⏳ Time Taken
- **Research & Analysis**: ~12 hours
- **Implementation & Testing**: Based on the output quality of both OCR technologies

---

## 🏗 Project Stages
### Stage 1: OCR Script
#### **Image Processing & Preprocessing**
- **Read Image**: Image is loaded and processed using the Pillow library.
- **Preprocessing**: Applied grayscale conversion and binary thresholding.
- **Noise Removal**: Medium blur used to enhance text clarity.
- **Morphological Operations**: Closing used to fill gaps in handwritten text.
- **Text Extraction**:
  - **pytesseract**: Works well on printed text but struggles with handwritten text.
  - **EasyOCR**: Performs better with handwritten text but has issues with submerged text.

#### **Text Structuring & Storage**
- **Regex Patterns**: Extract key fields from OCR results.
- **Dictionary Mapping**: Store extracted values in an organized dictionary.
- **JSON Output**: Format the structured data into JSON for further processing.

### Stage 2: Database Schema Design
- Designed a **MySQL schema** to store extracted patient details.
- Created **tables**:
  - **patient_table**: Stores basic patient information.
  - **form_data**: Stores JSON data extracted from OCR processing.
- Schema was designed using **MySQL Command Prompt** and later exported.

### Stage 3: MySQL Database Integration
- **Python-SQL Connection**: Established using `mysql-connector-python`.
- **JSON Data Handling**:
  - Read extracted JSON data.
  - Insert matching fields into the corresponding SQL tables.
- **Success Message**: Prints confirmation upon successful insertion.

---

## 📄 References & Documentation
- [Tesseract OCR GitHub Documentation](https://github.com/tesseract-ocr/tesseract)
- [EasyOCR Official Documentation](https://www.jaided.ai/easyocr/)
- [Stack Overflow Discussions on EasyOCR & Tesseract](https://stackoverflow.com/)

Warm Regards 

