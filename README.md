### PDF Extractor with Local LLM
This repository contains a Python project, encapsulated in a Jupyter Notebook (main.ipynb), designed for extracting information from PDFs and potentially processing images, leveraging a local Large Language Model (LLM) for advanced text understanding and generation.

## Features
- PDF Parsing: Utilizes pymupdf to extract content from PDF documents.

- Optical Character Recognition (OCR): Integrates pytesseract for extracting text from images within PDFs or standalone images.

- Image Processing: Employs Pillow and opencv-python for image manipulation and analysis, likely used in conjunction with OCR.

- Local LLM Integration: Leverages llama-cpp-python to run a local large language model (specifically, tinyllama-1.1b-chat-v1.0.Q6_K.gguf) for natural language understanding and generation tasks.

- Deep Learning Capabilities: Includes torch, torchvision, and torchaudio for potential deep learning-based image analysis or other tasks.


## Installation
To set up the environment and run the notebook, follow these steps:

1. Clone the repository:

``git clone <repository_url>``

``cd <repository_name>``


2. Create a virtual environment (recommended):

``python3.10 -m venv .venv``

``source .venv/bin/activate``


3. Install the required dependencies:
The main.ipynb notebook itself contains commands to install necessary libraries. You can run the first few cells of the notebook to install them automatically. These include:

``!python3.10 -m pip install --upgrade pip``

``!python3.10 -m pip install torch torchvision torchaudio``

``!python3.10 -m pip install transformers pymupdf pytesseract pillow``

``!python3.10 -m pip install --force-reinstall --no-cache-dir llama-cpp-python``

``!python3.10 -m pip install safetensors``

``!python3.10 -m pip install tqdm numpy opencv-python``


Note: The llama-cpp-python installation might require specific build tools depending on your operating system and hardware for optimal performance (e.g., Metal for macOS, CUDA for NVIDIA GPUs).

4. Download the LLM model:
This project uses tinyllama-1.1b-chat-v1.0.Q6_K.gguf. You will need to download this model file and place it in the appropriate directory (e.g., /pdf_extracter/ as indicated in the notebook output).

### Usage
1. Start Jupyter Notebook:
2. Open main.ipynb:
3. Navigate to and open the main.ipynb file in your browser.
3. Run the cells:
  - Execute the cells sequentially. The notebook is set up to:
  - Install all required Python packages.
  - Load the local LLM model (tinyllama-1.1b-chat-v1.0.Q6_K.gguf).
  - Process PDF documents (based on the installed libraries and observed output, it appears to extract text and potentially images).
  - Saved image outputs such as output1/page_3_img_1.png and output1/page_3_img_2.jpeg suggest that it can extract and save images from PDFs.

### Model Used
- tinyllama-1.1b-chat-v1.0.Q6_K.gguf: This is a quantized version of the TinyLlama 1.1B chat model, designed for efficient local inference using llama-cpp-python. It's suitable for various natural language processing tasks, including text summarization, question-answering, and content generation from the extracted PDF data.
