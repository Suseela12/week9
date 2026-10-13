# Experiment 9 : JSON Generation and Validation

## Aim
To generate structured JSON output using an LLM and validate its syntax and structure using Python.

## Problem Statement
Generate a JSON array containing exactly three book objects. Each object must contain the keys `title`, `author`, and `year`.

## Technologies Used
- Python
- Google Gemini AI
- Google Gen AI SDK
- JSON

## Algorithm
1. Initialize the Gemini API client.
2. Define a prompt requesting JSON-only output.
3. Send the prompt to the LLM using temperature 0.
4. Parse the response using `json.loads()`.
5. Validate the array length, required keys, and data types.
6. If validation fails, retry with a stricter prompt.
7. Print the validated JSON and save it to a file.

## Installation

```bash
pip install -r requirements.txt
```

## Configuration
Set the `GEMINI_API_KEY` environment variable before execution. Never upload API keys to GitHub.

## Execution

```bash
python src/main.py
```

## Expected Output
A valid JSON array containing three book objects, with `title` and `author` as strings and `year` as an integer.

The output is saved to `output/books.json`.

## Result
The experiment demonstrates how an LLM can generate structured JSON and how Python validation can detect invalid syntax, missing keys, incorrect data types, and an incorrect number of objects.

## Conclusion
Clear output instructions and programmatic validation improve the reliability of structured LLM output. Retrying with a stricter prompt can help correct errors, but every generated response must be validated before use.


└── README.md
```
