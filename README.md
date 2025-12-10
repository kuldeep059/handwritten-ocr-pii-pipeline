# handwritten-ocr-pii-pipeline
End-to-end Python pipeline for converting handwritten form images into text, automatically identifying, and preparing to redact PII (Personally Identifiable Information) using Tesseract OCR and spaCy.
a# OCR and PII Extraction Pipeline

## Project Objective
This project implements an end-to-end pipeline to process handwritten document images (JPEG) using Optical Character Recognition (OCR) and detect Personally Identifiable Information (PII) using spaCy.

## Pipeline Flow
1. **Input:** Handwritten JPEG document (`doc_a.jpg`, etc.)
2. **Pre-processing:** Uses OpenCV for Grayscale conversion and Adaptive Thresholding to enhance handwriting contrast.
3. **OCR:** Tesseract (v5.5.0, configured with PSM 4 for forms) extracts raw text.
4. **Text Cleaning:** Removes non-ASCII characters and excess whitespace.
5. **PII Detection:** Uses the `en_core_web_sm` spaCy model to detect entities like PERSON, DATE, and ORG.

## Setup and Dependencies
To run this project, you need:
1. Python 3.11
2. The Tesseract OCR application (v5.x) installed and added to your system PATH.
3. The necessary Python libraries listed in `requirements.txt`.

**To set up the environment:**
```bash
# 1. Create and activate environment
python3.11 -m venv ocr_pii_env
.\ocr_pii_env\Scripts\activate.ps1

# 2. Install Python dependencies
pip install -r requirements.txt

# 3. Download spaCy model
python -m spacy download en_core_web_sm

## 🚀 Step 2: Push to GitHub

Now that you have your code (`OCR_PII_Pipeline.ipynb`), your samples, `requirements.txt`, and `README.md`, you are ready to use Git.

**Action:** Execute the following commands in your PowerShell, **starting from your project directory**:

| Step | Command | Description |
| :--- | :--- | :--- |
| **1. Initialize** | `git init` | Turns your folder into a local Git repository. |
| **2. Add Files** | `git add .` | Stages ALL files in the current folder for the first commit (including your notebook, images, and `requirements.txt`). |
| **3. Commit** | `git commit -m "Initial commit of the OCR PII pipeline"` | Creates the first snapshot (commit) of your project. |
| **4. Create Remote Repo** | *Go to GitHub.com and create a **New Repository** (e.g., `ocr-pii-pipeline`). DO NOT initialize it with a README or license.* | |
| **5. Link Local to Remote** | `git remote add origin [YOUR_REPO_URL]` | Connects your local folder to the new GitHub repository (replace `[YOUR_REPO_URL]` with the HTTPS link from GitHub). |
| **6. Push** | `git push -u origin master` | Uploads your code to the GitHub website. |

After running these steps, refresh your GitHub repository page. All your files, including the complete Python Notebook, will be available online!
