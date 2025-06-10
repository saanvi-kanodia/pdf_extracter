# 📄 PDF Information Extraction System

## 🔍 Overview

This project is designed to extract structured and unstructured information from PDF documents. It supports:
- Text extraction using PyMuPDF (`fitz`)
- Image extraction from pages
- Image captioning using BLIP (Hugging Face)
- Page-level summaries using local LLaMA models (GGUF format)
- Clean output structure for easy inspection

## 🚀 Features

- 📄 **Text Extraction**: Pulls text from each page using PyMuPDF.
- 🖼️ **Image Extraction**: Converts each page to a high-res image.
- ✍️ **Image Captioning**: Describes images using BLIP captioning model.
- 🧠 **Page Summarization**: Generates 1–2 sentence summaries using local LLaMA models.
- 📂 **Structured Output**: Creates organized output folders for text, images, captions, and summaries.

## 🛠️ Requirements

Install the required libraries with:

pip install PyMuPDF pillow transformers torch llama-cpp-python
📁 Folder Structure
pgsql
Copy
Edit
project_root/
│
├── input/               # Folder for input PDF files
├── output/              # Output organized by document name
│   ├── extracted_text.txt
│   ├── image_captions.json
│   ├── page_summaries.json
│   └── summary.json
└── main.ipynb           # Main notebook with full logic
⚙️ Usage
Run main.ipynb step-by-step or convert it into a Python script. Make sure to place .gguf model (e.g., TinyLLaMA) in the working directory.

