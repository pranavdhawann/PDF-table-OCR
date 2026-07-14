# PDF-table-OCR

Extract tables from PDF documents and save the results as CSV files. The Google Colab notebook combines PDF rendering, Microsoft Table Transformer models, table-structure detection, and EasyOCR.

## PDF workflow

These repositories cover three complementary stages:

1. [PDF2IMAGE](https://github.com/pranavdhawann/PDF2IMAGE) converts PDF pages to images.
2. [PDF-table-OCR](https://github.com/pranavdhawann/PDF-table-OCR) detects, crops, and OCRs tables into CSV files.
3. [PDFInsightBot](https://github.com/pranavdhawann/PDFInsightBot) indexes PDF text locally and supports question answering with Ollama.

Use this project when the important content is structured data inside PDF tables.

## Features

- Render PDF pages to images
- Detect tables with Microsoft Table Transformer
- Recognize table structure and cells
- Run English OCR with EasyOCR
- Export combined and split table CSV files
- Package outputs as `table.zip` in Colab

## Run in Google Colab

1. Open [`table-detection-extraction.ipynb`](table-detection-extraction.ipynb) in Google Colab.
2. Mount Google Drive or use local Colab paths.
3. Update `config.json` with the PDF, image, table, and CSV paths.
4. Set the notebook's `config_path` to the location of that JSON file.
5. Run the cells from top to bottom. A GPU runtime is recommended.

The notebook installs its main dependencies, including `transformers`, `easyocr`, `pdf2image`, `torch`, `torchvision`, `pandas`, and `tabulate`. Poppler is also required for PDF rendering.

## Outputs

- Rendered page images under `images_path`
- Cropped table images and per-table CSV files under `tables_path`
- Combined CSV at `csv_path`
- Downloadable `table.zip`

## Project structure

```text
table-detection-extraction.ipynb   End-to-end Colab workflow
config.json                         Input and output paths
ast_sci_data_tables_sample.pdf     Sample PDF
Output/                             Example or generated output files
```

## License

MIT. See [LICENSE](LICENSE).