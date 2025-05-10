# rankPage: Simple Web Crawler & Search Engine

A lightweight, browser-based web crawler and search engine that allows you to index websites and search through their content.

![rankPage](https://api.dicebear.com/7.x/bottts/svg?seed=samantha)

## Features

- **Web Crawler**: Crawl websites starting from a URL with configurable depth and page limits
- **Domain Restriction**: Option to stay within the same domain during crawling
- **PageRank Algorithm**: Implements a simplified version of the PageRank algorithm to rank pages
- **Full-Text Search**: Search through crawled content with term highlighting
- **Data Management**: Save, load, export, and import crawled data
- **Statistics**: View crawl statistics and top-ranked pages

## How It Works

1. **Crawling**: Enter a starting URL, set crawl parameters, and begin crawling
2. **Indexing**: As pages are crawled, they are indexed and their content is analyzed
3. **Ranking**: Pages receive a rank based on their connectivity using a PageRank-inspired algorithm
4. **Searching**: Search through indexed content with relevance-based results

## Getting Started

### Method 1: Direct File Opening

1. Clone this repository
2. Open `index.html` in your web browser

### Method 2: Using a Local Server

For the best experience (avoiding CORS issues), use a local server:

```bash
# Using Python
python -m http.server

# Using Node.js with http-server
npx http-server
```

## Usage

### Crawling

1. Enter a starting URL in the "Start URL" field (or select from provided starter links)
2. Set the maximum crawl depth (how deep to follow links)
3. Set the maximum number of pages to crawl
4. Choose whether to stay on the same domain
5. Click "Start Crawling"

### Searching

1. Enter search terms in the search box
2. Results will be displayed with relevance ranking and highlighted terms

### Data Management

- **Save Data**: Save current crawl data to browser localStorage
- **Load Data**: Load previously saved data from localStorage
- **Export Data**: Download crawl data as a JSON file
- **Import Data**: Load crawl data from a previously exported JSON file
- **Clear Data**: Reset all crawl data

## Technical Details

- Built using pure vanilla JavaScript, HTML, and CSS (with Bootstrap for UI)
- Uses the browser's localStorage for data persistence
- Implements a simplified PageRank algorithm
- Uses a CORS proxy (AllOrigins) to fetch content from different domains
- Single-file application with no external dependencies

## Limitations

- Browser-based crawling is limited by CORS restrictions (handled via proxy)
- Performance may degrade with very large crawls (recommended limit: 1000 pages)
- Some websites may block crawler access

## License

MIT

## Author

Created by Sammy Lord, with help from Samantha the AI.

---

*Note: This is a demonstration project intended for educational purposes. Please respect websites' robots.txt files and crawl policies when using this tool.* 
