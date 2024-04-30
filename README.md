# OCR Text Data Processing Pipeline

## Overview
This repository implements a pipeline to process text data extracted via OCR from laboratory test results or medical records. The goal is to transform unstructured OCR text into a structured Python list of dictionaries, adhering to the specified format:
[
    {"parameter": "iron", "value": 5.3, "unit": "mmol/mL"},
    # Additional dictionaries for other parameters...
]
### Objective
The objective of this project is to develop a pipeline, utilizing either a rule-based or NLP-based approach, that processes OCR text data and extracts relevant information such as parameters, values, and units. By transforming unstructured OCR output into structured Python dictionaries, this pipeline aims to facilitate further analysis and interpretation of laboratory test results or medical records.
