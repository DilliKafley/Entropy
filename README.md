' OCR Text Data Processing Pipeline

' Overview:
' This project implements a pipeline to process text data extracted via OCR from laboratory test results or medical records. The goal is to transform unstructured OCR text into a structured Python list of dictionaries, adhering to the specified format.

' Objective:
' The objective of this project is to develop a pipeline, utilizing either a rule-based or NLP-based approach, that processes OCR text data and extracts relevant information such as parameters, values, and units. By transforming unstructured OCR output into structured Python dictionaries, this pipeline aims to facilitate further analysis and interpretation of laboratory test results or medical records.

' Approach:
' The pipeline consists of several functions:
' - `convert_json_to_dict`: Loads JSON data containing abbreviations and synonyms, and converts it into a dictionary for easy lookup.
' - `extracted_list`: Processes OCR text data and extracts relevant information using regular expressions.
' - `extract_items`: Matches extracted text against abbreviations and synonyms to identify relevant items.
' - `replace_words_in_list`: Replaces abbreviations and synonyms in extracted items with their corresponding full forms.
' - `convert_to_dict`: Converts extracted items into dictionaries with keys for parameter, value, and unit.
' - `handle_units`: Handles special cases in units, such as removing digits from parameters and converting digits-only units to 'NA'.

' Usage:
' To use the pipeline, provide the paths to the JSON file containing abbreviations and synonyms, and the OCR file containing the text data. Call the `process_ocr` function with these paths as arguments, and the pipeline will return a structured Python list of dictionaries with extracted information.

' Contributing:
' Contributions to this project are welcome. If you have suggestions for improvements or new features, please open an issue or submit a pull request.

' License:
' This project is licensed under the MIT License.

' Contact:
' For questions or feedback regarding this project, please contact [Your Name](mailto:dillikafley25@gmail.com).

