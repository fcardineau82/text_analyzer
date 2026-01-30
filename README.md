````md
# Text Analyzer

A small Python CLI script that computes linguistic statistics and readability metrics (including **Flesch Reading Ease**) for a given piece of text.

## Features

- **Readability scoring**: Flesch Reading Ease
- **Basic stats**: word / sentence / syllable counts
- **Lexical diversity**: unique word fraction
- **Stylistic signals**: counts of common dialogue tags (e.g., *said/told*), conjunctions, WH-adverbs
- **Text normalization**: basic cleaning + ASCII conversion

---

## Quickstart

### 1) Clone

```bash
git clone https://github.com/fcardineau82/text_analyzer.git
cd text_analyzer
````

### 2) (Recommended) Create a virtual environment

```bash
python -m venv .venv
source .venv/bin/activate   # macOS / Linux
# .venv\Scripts\activate    # Windows
```

### 3) Install dependencies

```bash
pip install -r requirements.txt
```

> Note: If you see an NLTK resource error on first run, install the required tokenizer data (commonly `punkt`):
>
> ```bash
> python -m nltk.downloader punkt
> ```

---

## Usage

Pass the text directly as an argument:

```bash
python text_analyzer.py "Enter the text you want to analyze here."
```

Tip for longer text (macOS/Linux):

```bash
python text_analyzer.py "$(cat path/to/file.txt)"
```

Tip for Windows PowerShell:

```powershell
python text_analyzer.py (Get-Content -Raw path\to\file.txt)
```

---

## Output

The script prints a set of computed metrics to stdout (e.g., readability score, counts, and style indicators).

---

## Technical note (Flesch Reading Ease)

Flesch Reading Ease is computed as:

```
206.835
  - 1.015 * (words / sentences)
  - 84.6  * (syllables / words)
```

---

## Credits

Inspired by the methodologies in *Building Machine Learning Powered Applications* by Emmanuel Ameisen.

---

## License

MIT — see [LICENSE](LICENSE).

```
::contentReference[oaicite:0]{index=0}
```
