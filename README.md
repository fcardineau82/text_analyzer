# Text Analyzer

A Python CLI tool that provides linguistic statistics, word usage analysis, and readability scores. It processes raw text to evaluate stylistic choices and reading complexity.

## Features

* **Readability Scoring:** Implements the Flesch Reading Ease algorithm.
* **Linguistic Statistics:** Counts total words, sentences, and syllables.
* **Lexical Diversity:** Calculates the unique word fraction to measure vocabulary richness.
* **Stylistic Analysis:** Tracks usage of dialogue tags (told/said), conjunctions, and WH-adverbs.
* **Text Normalization:** Handles ASCII conversion and basic cleaning.

## Installation

1. **Clone the repository:**
```bash
git clone https://github.com/fcardineau82/text_analyzer.git
cd text-analyzer

```


2. **Install dependencies:**
```bash
pip install nltk

```



## Usage

Run the script by passing the input text as a command-line argument:

```bash
python analyzer.py "Enter the text you want to analyze here."

```

## Technical Details

The Flesch Reading Ease score is calculated using the following formula:

206.835 - 1.015 * (number_of_words / number_of_sentences) - 84.6 * (number_of_syllables / number_of_words)

## Credits

Inspired by the methodologies in **"Building Machine Learning Powered Applications"** by Emmanuel Ameisen.
