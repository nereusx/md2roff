# md2roff

A simple, lightweight Markdown to roff (man ms) converter.  
Ideal for transforming Markdown-formatted documentation (like `README.md`) into UNIX manual pages or compatible HTML.

---

## Features

- Converts Markdown into **roff-format man pages** (`man(7)` style) and/or **HTML**.
- Supports basic Markdown constructs: headings, paragraphs, lists, code blocks, etc.
- Lightweight and dependency-light—built using a simple lexer/parser approach (e.g., flex & C).
- Includes a Makefile for easy building and installation.
- Optional: ability to output to PDF or PostScript using external tools (like `groff`, `troff`, etc.).

---

## Prerequisites

- C99-compatible compiler (e.g., `gcc`)
- `make` (GNU Make or equivalent)
- `lex` or compatible lexer generator (e.g., `flex`)

---

## Quick Start

```sh
# Build the tool
make

# Example usage:
./md2roff README.md | groff -ms -Tpdf > output.pdf
