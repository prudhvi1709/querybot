# QueryBot

A powerful web application that enables users to upload various data formats, execute SQL queries, and download results through an intuitive interface.

## Overview

QueryBot is built with FastAPI for the backend and a responsive HTML/Bootstrap frontend. It provides a seamless experience for data analysis by allowing users to query multiple data sources through a unified SQL interface.

## Features

- **Multi-format Support**: Query CSV, Parquet, SQLite, Excel files, and MySQL databases with a single interface
- **Interactive SQL Editor**: Writes and executes SQL queries with syntax highlighting. The application automatically generates DuckDB queries and runs on datasets. It supports multiple files if the paths are provided separated by commas.
- **Real-time Results**: View query results instantly in a paginated table format
- **Export Functionality**: Download query results in CSV format for further analysis
- **Responsive Design**: Works seamlessly across desktop and mobile devices

## Getting Started

### Installation

```bash
pip install querybot
```

### Running the Application

1. Start the application with a single command using `uv`:
   ```bash
   uvx querybot
   ```
2. Open your web browser and navigate to [http://localhost:8001](http://localhost:8001) to access the QueryBot interface.

### Usage

1. **Upload Data**: Use the interface to specify data sources by:
   - Entering file paths (multiple paths can be separated by commas, without quotes)
   - Uploading files directly through the browser

2. **Supported Data Formats**:
   - CSV files (`.csv`)
   - Parquet files (`.parquet`)
   - SQLite databases (`.db`)
   - Excel spreadsheets (`.xlsx`)
   - External MySQL databases (from relational-data.org)

3. **Execute Queries**: Write SQL queries in the editor and click "Run Query" to see results.

4. **Export Results**: Download query results as CSV files for further analysis or reporting.

## Project Structure

```
/querybot
│
├── querybot              # Main package directory
│   ├── app.py            # FastAPI application entry point
│   ├── __init__.py       # Package initialization
│   ├── static            # Static assets
│   │   ├── index.html    # Main frontend interface
│   │   └── js            # JavaScript resources
│   │       └── script.js # Frontend functionality
├── pyproject.toml        # Project metadata and dependencies
├── .gitignore            # Git ignore configuration
├── uv.lock               # Dependency lock file
├── README.md             # Project documentation
```

## Development

### Prerequisites

- Python 3.8+

### Setting Up Development Environment

1. Clone the repository:
   ```bash
   git clone https://github.com/gramener/querybot.git
   cd querybot
   ```

2. Install dependencies:
   ```bash
   pip install -e ".[dev]"
   ```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Additional Resources

- [QueryBot on PyPI](https://pypi.org/project/querybot/)
- [Issue Tracker](https://github.com/gramener/querybot/issues)

## Query Result

![Query Result](Screenshot.png)