## 2025-05-22 - Input Validation and Safety Checks for Image Processing
**Vulnerability:** Lack of input validation for user-provided ROI configuration and potential division by zero during image normalization in `mtf_computer.py`.
**Learning:** Even when using "safe" parsing like `ast.literal_eval`, subsequent logic can still fail if the structure or values are unexpected. Robust validation of the parsed dictionary keys and value types is essential.
**Prevention:** Always validate the schema and values of parsed data. Use safety checks (e.g., checking for zero or NaN) before performing normalization or other numerical operations on arrays derived from external sources.
