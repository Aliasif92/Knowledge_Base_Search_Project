# kbsearch

A local knowledge-base indexer and full-text search CLI that turns a folder of notes into a fast, queryable index.
It uses SQLite FTS5 under the hood, so it is portable, fast, and requires no external services.

## Why this is a good GitHub portfolio project

This repository showcases:

- Modern packaging (`pyproject.toml`, `src/` layout, console scripts)
- A clean architecture (extractors → indexer → search service → CLI)
- Type hints and static typing (`mypy`-friendly)
- Robust error handling and structured logging
- SQLite schema management and FTS5 querying
- Async file watching (`watchfiles` + `asyncio`)
- Automated tests + CI (GitHub Actions)

## Features

- Initialize an index database
- Index a folder of files (`.md`, `.markdown`, `.txt`)
- Incremental re-indexing (skips unchanged files via SHA-256)
- Full-text search with snippets and ranking
- Watch mode that updates the index on file changes
- Export search results to JSON or CSV

## Quick start

### 1) Install

From the project root:

```bash
python -m venv .venv
# Linux/macOS:
source .venv/bin/activate
# Windows (PowerShell):
# .venv\Scripts\Activate.ps1

pip install -U pip
pip install -e ".[dev]"
