# vector_embedding

This code appears to be a Python script for extracting and analyzing information from HTML files, particularly related to web page elements (e.g., buttons, links, forms) and their corresponding text content. Let's break down the main components and functionality of the code:

Libraries Used:
sys: Standard library for system-specific parameters and functions.
lxml: Library for processing XML and HTML.
numpy (as np): Library for numerical operations, used for vector manipulation.
spacy: Natural Language Processing library. It loads the "en_core_web_lg" model for English language processing.
pickle, re, json, os: Standard libraries for handling data serialization, regular expressions, JSON, and operating system-related tasks.
sklearn: Library for machine learning tasks. In this code, it is used for calculating cosine similarity.
Classes:
Node: Represents an HTML element. It has methods for extracting information, generating vectors, and determining the type of HTML element.
Html2Vec: Takes HTML content as input and converts it into a list of Node objects. It uses spaCy to generate vectors for each HTML element.
UIMapper: Uses Html2Vec to map UI elements from HTML content.
ReportGenerator: Generates a report containing information about HTML elements, including cosine similarity with a user-input vector.
Main Code Flow:
User Input:

The user provides input text for a UI element (function get_user_input_text).
The input text is converted into a vector using spaCy.
HTML Processing:

HTML files in a specified directory are processed.
For each HTML file, a report is generated using ReportGenerator.generate_report.
The report includes information about HTML elements, their vectors, types, actual names, and cosine similarity with the user input vector.
Cosine Similarity Calculation:

Cosine similarity is calculated between the user input vector and vectors of HTML elements.
The HTML element with the highest cosine similarity is identified for each HTML file.
Overall Best Matching Entry:

The overall best matching entry across all HTML files is identified based on the highest cosine similarity.
Printing and Opening Results:

Details of the best matching entries are printed, including node type, actual name, category, XPath, and vector.
The HTML file with the overall best match is opened in the default web browser.
