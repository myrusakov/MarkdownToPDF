# Markdown/GitBook to PDF Converter

This project allows you to convert Markdown (.md) files into a single PDF document with support for styles and formatting. The program uses `pdfkit` (which wraps `wkhtmltopdf`) for generating PDF and `markdown2` for converting Markdown to HTML. It is suitable for GitBook repositories.

## Key Features
- Conversion of all Markdown files in the directory into a single PDF document.
- Automatic removal of metadata, if present, from each Markdown file created in GitBook.
- Syntax highlighting for code.
- HTML processing (optional) for better formatting.

## Installation

1. Make sure you have Python version 3.x installed.
   - [Download Python](https://www.python.org/downloads/)
2. Make sure you have `wkhtmltopdf` installed.
   - [Download wkhtmltopdf](https://wkhtmltopdf.org/downloads.html)
3. Install the Python dependencies:
   ```bash
   pip install markdown2 pdfkit
   ```
	
## Configuration

Configure the variables at the beginning of the script:

- `repo_path`: the path to the directory with Markdown files.
- `output_pdf_path`: the path to save the output PDF file.
- `excluded_files`: Markdown files that should not be included in the PDF.
- `debug_html`: if `True`, a debug HTML file will be created.
- `include_page_break`: if `True`, adds a page break between files.
- `enable_html_processing`: if `False`, disables additional HTML processing.

## Usage

1. Ensure all dependencies are installed, including `markdown2` and `pdfkit`.
2. Configure the variables at the beginning of the script (see the [Configuration](#Configuration) section).
3. Optionally, configure the `style.css` file for styling your PDF.
4. Run the script with the command:
   ```bash
   python main.py
   ```
5. After the script runs, the output PDF file will be saved at the path specified in `output_pdf_path`.

Optionally: If `debug_html` is set to `True`, a debug HTML file named `debug.html` will be generated.
