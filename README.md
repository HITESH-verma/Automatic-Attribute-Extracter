# Automatic-Attribute-Extracter

Goal:
Extract product attributes (e.g., weight, voltage, ingredients) from images using OCR.

Steps:

1. Set Up Environment
   - Install: pytesseract, opencv-python, pandas
   - Install Tesseract OCR and configure its path

2. Load Image
   - Use OpenCV to read and preprocess image (grayscale, thresholding)

3. Apply OCR
   - Use Tesseract with config: --psm 11 --oem 1
   - Extract raw text from the image

4. Clean Text
   - Replace newline characters, fix spacing

5. Extract Attributes
   - Use regex to find keywords like:
     - Weight (e.g., “500g”)
     - Voltage (e.g., “230V”)
     - Volume (e.g., “100ml”)
     - Ingredients (from block text)

6. Save Output
   - Save structured results to sample_test_out.csv
   - Save failed/partial results to sample_test_out_fail.csv

Tools Used: Python, OpenCV, Tesseract, Pandas
Use Case: Automating data entry from product packaging

