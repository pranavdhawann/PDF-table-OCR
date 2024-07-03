# pdf-table-ocr

A tool for extracting tables from PDF documents, performing OCR, and saving the tables as CSV files.

## Table of Contents

- [Overview](#overview)
- [Installation](#installation)
- [Usage](#usage)
  - [Requirements](#requirements)
  - [Running the Script](#running-the-script)
- [Project Structure](#project-structure)
- [Acknowledgments](#acknowledgments)
- [License](#license)

## Overview

This project automates the extraction of tables from PDF documents and converts them into CSV files using a series of steps:

1. **PDF to Image Conversion**: Converts PDF pages to images using `pdf2image`.
2. **Table Detection**: Detects tables in images with Hugging Face's `AutoModelForObjectDetection`.
3. **Table Cropping**: Crops detected tables from images.
4. **Structure Recognition**: Identifies table structure using `TableTransformerForObjectDetection`.
5. **OCR Processing**: Extracts text from table cells with EasyOCR.
6. **CSV Export**: Compiles extracted table data and saves it as CSV files.

The project leverages PyTorch, torchvision, PIL, pdf2image, and other libraries to achieve seamless integration and processing.

## Installation

Follow these steps to set up the project:

1. Clone the Repository:
   ```bash
   git clone https://github.com/pranavdhawann/pdf-table-ocr.git
   cd pdf-table-ocr
   ```
2. Install the required packages:
    ```bash
    !pip install transformers easyocr pdf2image
    !apt-get install poppler-utils
    ```
    
## Usage

### Requirements

1. transformers==4.30.2
2. torch==2.0.1
3. torchvision==0.15.2
4. Pillow==9.5.0
5. pdf2image==1.16.3
6. huggingface-hub==0.15.1
7. matplotlib==3.7.1
8. numpy==1.24.4
9. tqdm==4.65.0
10. easyocr==1.7.0
11. tabulate==0.9.0
12. pandas==2.0.3

### Running the Script

1. **Set Up Paths**:
    ```python
    pdf_path = '' 
    images_path = '/content/images'
    csv_path = '/content/Table.csv'
    tables_path = '/content/tables'
    ```

2. **Prepare Directories**:
    ```bash
    !mkdir /content/images
    !mkdir /content/tables
    ```

3. **Run the rest**
    
## Project Structure

├── images/ # Directory where images from the PDF are stored

├── tables/ # Directory where extracted tables will be saved

├── Table.csv # Output CSV file containing the extracted table data

├── script.py # Main script for extracting tables and performing OCR

└── README.md # This README file

## Acknowledgments

- [Hugging Face](https://huggingface.co/) for the `transformers` library and pre-trained models.
- [EasyOCR](https://github.com/JaidedAI/EasyOCR) for the OCR functionality.
- [Poppler](https://poppler.freedesktop.org/) for PDF processing.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
