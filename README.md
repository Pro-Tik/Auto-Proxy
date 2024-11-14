# Auto-Proxy
# Proxy Downloader and Formatter

This script is designed to load proxy URLs from a file, download proxies from those URLs, format them with authentication information, and save them into a new file.

## Features
- **Load Proxy URLs**: Loads a list of proxy URLs from a specified text file (`auth.txt`).
- **Download Proxies**: Downloads proxy data from the provided URLs and stores the proxies in a list.
- **Reformat Proxies**: Reformats each proxy by adding the proxy type (`http://username:password@ip:port`).
- **Save Proxies**: Saves the formatted proxies to a text file (`proxies.txt`).

## Requirements
- Python 3.x
- `requests` library (can be installed using `pip install requests`)

## How It Works
1. **Load Proxy URLs**: The script reads proxy URLs from a text file (default: `auth.txt`). Each URL is expected to point to a source where proxies are listed.
2. **Download Proxies**: The script then downloads the proxy data from these URLs. Each URL should return a list of proxies in `ip:port:username:password` format.
3. **Reformat Proxies**: The proxies are reformatted to include the `http://` scheme and authentication details in the form of `http://username:password@ip:port`.
4. **Save Formatted Proxies**: The final list of formatted proxies is saved to a new text file (`proxies.txt`).

## Usage

### Step 1: Prepare Your Proxy URLs File
Create a file named `auth.txt` and add the proxy URLs that return proxy data in `ip:port:username:password` format.

Example of `auth.txt`:

