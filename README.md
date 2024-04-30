# OCR Text Data Processing Pipeline

## Overview
This project implements a pipeline to process text data extracted via OCR from laboratory test results or medical records. The goal is to transform unstructured OCR text into a structured Python list of dictionaries, adhering to the specified format:
```python
[
    {"parameter": "iron", "value": 5.3, "unit": "mmol/mL"},
    # Additional dictionaries for other parameters...
]
