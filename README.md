# EPUB Scraper

A python script that scrapes novels from NovelFire, fetches all available chapters, and compiles them into neatly structured EPUB files for offline reading.

## Features

- Fetches all chapters of a novel.
- Automatically paginates through chapter lists.
- Extracts clean chapter content (removing scripts/styles).
- Creates EPUB files, dividing chapters into volumes (configurable).
- Adds metadata like titles, chapters, and a table of contents.

## Requirements

- Python 3.8+
- beautifulsoup4
- ebooklib

## Installation

1. Clone the repository
2. Install depedencies:
```bash
pip install requests beautifulsoup4 ebooklib
```

## Usage

1. Run the bot:
```bash
python novel_scraper.py
```
2. Fill out the prompted inputs
    - Book Name – The name from the novel’s URL (e.g., for https://novelfire.net/book/shadow-slave, enter shadow-slave).
    - Chapters per EPUB – (Optional) Number of chapters per EPUB file (default is 100).
    - Delay between requests – (Optional) Delay in seconds between HTTP requests (default is 1).

## Output

The script saves generated .epub files in a folder called epub_output/.
```sraper-repl
epub_output/
├── shadow-slave-volume-1.epub
├── shadow-slave-volume-2.epub
...
```

## Known Issues

- The script assumes a consistent HTML structure on NovelFire. If the website changes, the scraper may break.
- Some chapters may be skipped if content is not found or an error occurs during fetching.

## Todo

- Support other novel websites.
- Better error handling and retry logic.

## License

This project is licensed under the MIT License.