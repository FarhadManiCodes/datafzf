# DataFZF

> FZF-powered tools for exploring and analyzing data files.

Hi, DataFZF is my personal side project—a collection of tools written in Go to help me navigate, search, and profile data files more easily from the terminal. It pulls together things I often used in separate scripts and wraps them with an FZF-powered interface.

## Highlights

* 📁 Browse and preview data files quickly (CSV, JSON, YAML, etc.)
* 🔍 Search file contents and structure (columns, data types, etc.)
* 🧪 Run simple data profiling (via Python backends)
* ⚡ Fast and responsive thanks to Go + parallelism

## Requirements

* Go 1.21+
* fzf
* Python 3.8+ (for profiling)
* Optional: `bat`, `jq`, `fd`, `ripgrep`, `qsv`

## Install

```bash
# From release
curl -L https://github.com/FarhadManiCodes/datafzf/releases/latest/download/datafzf-linux-amd64.tar.gz | tar xz
sudo mv datafzf /usr/local/bin/

# Or build from source
git clone https://github.com/FarhadManiCodes/datafzf.git
cd datafzf
go build -o datafzf cmd/datafzf/main.go
```

## Example Usage

```bash
# Browse files with preview and stats
datafzf data

# Search for column names like 'email'
datafzf search --data "contains:email"

# Quick file preview
datafzf preview file.csv

# Profile CSV file (Python required)
datafzf profile data.csv
```

## Why?

I built this to simplify working with messy data files scattered across directories. I use it daily for:

* Quickly previewing structure before opening files
* Searching for relevant data assets by schema or content
* Running quick checks or profiling before deeper analysis

It's still early stage and evolving as I experiment more. Feedback welcome if you try it!

## License

MIT

---
