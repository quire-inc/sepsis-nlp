# Sepsis NLP
Each file contains multiple regular expressions, one per line.  

Compatible with Python **re** module using **re.IGNORECASE** flag.

<!-- [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)]() -->

## Python Example
<!--<summary>Advanced: streaming results</summary>-->
```python
import re
from pathlib import Path

# Read text to be searched
text = Path("path/to/file.txt").read_text(encoding="utf-8")

# Read regex lines from file and combine into one regex string, with each expression separated by a "|" 
regex_lines = Path("regex-python-infection.txt").read_text(encoding="utf-8").splitlines()
regex = "|".join(regex_lines)

re.search(regex, text, re.IGNORECASE)
```
