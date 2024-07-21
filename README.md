# Table Detection and Extraction from PDF

Detect and Extract tables from PDF documents and save to .csv file.

## Table of Contents

- [Features](#features)
- [Requirements](#requirements)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Features

- Convert PDF pages to images
- Detect tables and table structures using pretrained models
- Crop and extract detected tables
- Perform OCR on table cells
- Save extracted tables as CSV files
  
## Requirements

- Python 3.x
- Google Colab (for running the code)
- Required Python packages:
  - transformers
  - easyocr
  - pdf2image
  - torch
  - torchvision
  - matplotlib
  - numpy
  - pandas
  - tabulate
    
## Usage

1. Install required packages:

    ```bash
    !pip install transformers easyocr pdf2image
    !apt-get install poppler-utils
    ```

2. Update `config.json` with your file paths:

    ```json
    {
      "pdf_path": "",
      "csv_path": "",
      "images_path": "",
      "tables_path": ""
    }
    ```
        
## Project Structure

├── tables/ # Directory where extracted images and tables will be saved

├── script.py # Main script for extracting tables and performing OCR

└── README.md # This README file

## Acknowledgments

- [Hugging Face](https://huggingface.co/) for the `transformers` library and pre-trained models.
- [EasyOCR](https://github.com/JaidedAI/EasyOCR) for the OCR functionality.
- [Poppler](https://poppler.freedesktop.org/) for PDF processing.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
