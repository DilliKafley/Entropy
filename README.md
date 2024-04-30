# OCR Text Data Processing Pipeline

## Overview
This repository implements a pipeline to process text data extracted via OCR from laboratory test results or medical records. The goal is to transform unstructured OCR text into a structured Python list of dictionaries, adhering to the specified format:
```python
[
    {"parameter": "iron", "value": 5.3, "unit": "mmol/mL"},
    # Additional dictionaries for other parameters...
]
```
### Objective
The objective of this project is to develop a pipeline, utilizing either a rule-based or NLP-based approach, that processes OCR text data and extracts relevant information such as parameters, values, and units. By transforming unstructured OCR output into structured Python dictionaries, this pipeline aims to facilitate further analysis and interpretation of laboratory test results or medical records.

## Key Considerations

- **Data Unstructuredness and OCR Faults:** The input data will be highly unstructured with potential inaccuracies due to OCR errors.
- **Uniformity in Units and Parameter Names:** Ensure that units and parameter names match the specifications in the attached file X1.
- **Parameter Uniqueness:** Each parameter name must be unique within the dataset, discarding duplicates and retaining only the first instance.
- **Date Sensitivity:** Focus solely on the latest test results, disregarding earlier data to ensure relevance and accuracy.
- **Data Integrity:** Aim for a data integrity level exceeding 90% to ensure reliability.


# Approch
' The pipeline consists of several functions:
' - `convert_json_to_dict`: Loads JSON data containing abbreviations and synonyms, and converts it into a dictionary for easy lookup.
' - `extracted_list`: Processes OCR text data and extracts relevant information using regular expressions.
' - `extract_items`: Matches extracted text against abbreviations and synonyms to identify relevant items.
' - `replace_words_in_list`: Replaces abbreviations and synonyms in extracted items with their corresponding full forms.
' - `convert_to_dict`: Converts extracted items into dictionaries with keys for parameter, value, and unit.
' - `handle_units`: Handles special cases in units, such as removing digits from parameters and converting digits-only units to 'NA'.


# Usage
To use the pipeline, provide the paths to the JSON file containing abbreviations and synonyms, and the OCR file containing the text data. Call the process_ocr function with these paths as arguments, and the pipeline will return a structured Python list of dictionaries with extracted information.

```python
import json
from process_ocr import process_ocr

json_path = "abbreviations.json"
ocr_path = "text_data.txt"

output_data = process_ocr(json_path, ocr_path)
for item in output_data:
    print(f"Parameter: {item['parameter']}, Value: {item['value']}, Unit: {item['unit']}")
```
# Contributing
Contributions to this project are welcome. If you have suggestions for improvements or new features, please open an issue or submit a pull request.

# License
This project is licensed under the MIT License.

# Contact
For questions or feedback regarding this project, please contact [Dilli kafley](mailto:dillikafley25@gmail.com).
