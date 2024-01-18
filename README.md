# Medical Data Extraction Project Readme

## Overview

This project involves the extraction of medical data from PDF documents containing patient details and prescribed medicines. The workflow includes converting the PDF documents into images and utilizing the OpenCV library for image processing. The extracted information is then made accessible through a web-based API using FastAPI, and the system can be interacted with using Postman.

## Dependencies

Make sure to install the following Python libraries and dependencies:

- pdf2image==1.10.0
- pytesseract==0.3.0
- opencv_python==4.1.2.30
- numpy==1.19.4
- pandas==0.25.3
- Pillow==7.0.0
- fastapi[all]

You can install these dependencies using the following command:

```bash
pip install pdf2image==1.10.0 pytesseract==0.3.0 opencv_python==4.1.2.30 numpy==1.19.4 pandas==0.25.3 Pillow==7.0.0 "fastapi[all]"
```

## Workflow

1. **PDF to Image Conversion:**
   - The PDF documents containing patient details and medicines are converted into images using the `pdf2image` library.

2. **Image Processing with OpenCV:**
   - The OpenCV library is used for image processing to extract relevant information from the images.

3. **Text Extraction with Tesseract:**
   - The `pytesseract` library is employed to perform OCR (Optical Character Recognition) for extracting text information from the images.

4. **Data Representation:**
   - The extracted data is structured and represented in a format suitable for further processing. This may involve using NumPy arrays or Pandas DataFrames, depending on the nature of the data.

5. **Web API Development with FastAPI:**
   - FastAPI is used to develop a web-based API that provides access to the extracted medical data. The API endpoints allow users to query and retrieve specific information.

6. **Publication with Postman:**
   - The API is published on the web and can be interacted with using Postman. Postman can be used to send requests to the API endpoints and receive the extracted medical data in response.

## Usage
![Output Image 1](./images/riddhi.png)

1. Install the required dependencies as mentioned above.

2. Execute the script that performs the PDF to image conversion, image processing, and text extraction.

3. Run the FastAPI server to expose the API endpoints. You can do this by running the following command:

   ```bash
   uvicorn main:app --reload
   ```

4. Use Postman to send requests to the API endpoints and retrieve the extracted medical data
