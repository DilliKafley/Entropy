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

\section{Key Considerations}
\begin{itemize}
    \item \textbf{Data Unstructuredness and OCR Faults}: The input data will be highly unstructured with potential inaccuracies due to OCR errors.
    \item \textbf{Uniformity in Units and Parameter Names}: Ensure that units and parameter names match the specifications in the attached file X1.
    \item \textbf{Parameter Uniqueness}: Each parameter name must be unique within the dataset, discarding duplicates and retaining only the first instance.
    \item \textbf{Date Sensitivity}: Focus solely on the latest test results, disregarding earlier data to ensure relevance and accuracy.
    \item \textbf{Data Integrity}: Aim for a data integrity level exceeding 90\% to ensure reliability.
\end{itemize}
