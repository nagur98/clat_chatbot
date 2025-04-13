# clat_chatbot
Summary of the Approach
1. Tech Stack
Language: Python

Library: spaCy (used for NLP processing)

2. Knowledge Base (KB)
A small dictionary is defined with topics relevant to CLAT (e.g., syllabus, cut-off, exam pattern). Keys are phrases like "syllabus" or "marking scheme" and the values are detailed responses.

knowledge_base = {
    "syllabus": "The CLAT 2025 syllabus includes...",
    "exam pattern": "The CLAT exam has 150 multiple choice questions...",
    ...
}
3. NLP Preprocessing
Loads en_core_web_sm from spaCy.

Uses nlp() to tokenize and process user input.

4. Answer Matching Logic
Converts both input and KB keys to lowercase.

First, checks for all words in key being present in the user query.

If no exact match, falls back to checking for individual token matches from the input.

If no matches, returns a default fallback response.

5. CLI Chat Loop
A loop allows users to interact with the bot until they type exit, quit, or bye.
setup instructions

1. Python Environment
Python Version: >=3.7 (recommended: Python 3.8 or 3.9)

2. Required Libraries
You’ll need the following Python packages:

Package	Version	Purpose
* spacy	>=3.0.0	Natural Language Processing
* en_core_web_sm	compatible with spaCy version	English NLP pipeline (tokenization, POS, etc.)

3. Install the required libraries
pip install spacy
python -m spacy download en_core_web_sm
