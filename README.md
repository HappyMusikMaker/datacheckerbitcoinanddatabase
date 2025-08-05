# For further information, send me a message at andreas.contact.office@gmail.com.

# datacheckerbitcoinanddatabase
Bitcoin Private Key Navigator is an offline HTML page-by-page viewer; DataChecker is a Python CLI for generating, analysing or searching Bitcoin keys; Key-SiteFinder shows where a key sits in the database. All run unchanged on Windows or Ubuntu.

# Screenshots
![Screenshot 063836](./Screenshot%202025-08-05%20063836.png)
![Screenshot 063852](./Screenshot%202025-08-05%20063852.png)

# Bitcoin Private Key Navigator (Wide HTML) — English UI

A single-file, no-backend explorer that lets you **jump to any Bitcoin private
key, page-by-page, entirely inside your browser**.  All math happens locally,
so the page works offline and never sends data out.

## Quick start

Just open `Bitcoin_Database_en.html` in any modern browser.  
No internet? No problem — it’s self-contained.

## Key features

| Action | How |
| ------ | --- |
| **Go to page** | Enter a page number and hit **Go**. |
| **Random page** | Click **Lucky Draw** for a cryptographically random page. |
| **Search key** | Paste a 256-bit binary, 64-char hex, or (un)compressed WIF. The tool jumps to the correct page and highlights the matching row. |
| **Rows per page** | Change the number (1 – 1000) and hit **Apply**. |
| **Navigation** | **Previous** / **Next** buttons or manual page input. |

Each row displays:

1. Private Key (WIF uncompressed)  
2. Private Key (integer)  
3. Private Key (hex uncompressed)  
4. Public Address (uncompressed)  
5. Public Key (uncompressed)  
6. Hash160 (hex)  
7. Hash160 (integer)

## Safety notes

* These keys are **generated on-the-fly** and **not suitable for real funds**.
* Because everything runs client-side, the file is safe to keep offline.
* If you save/copy any keys, treat them as secrets.

Enjoy the English makeover — and happy key exploring! 🔑🚀

# DataChecker (English UI)

A multi-purpose Bitcoin key-tool that does **not** store any private data outside the CSV files you create.  
This version simply translates every prompt, menu entry, and user-facing text from German to English.  
All cryptographic logic, file formats, and command-line behaviour stay exactly the same.

## Features

| Mode | What it does |
|------|--------------|
| **1** | Manual key inspection – enter a private key, get WIF, address, Hash160, etc. |
| **2** | Generate *n* random private keys in parallel and store full datasets. |
| **3** | Generate *n* sequential keys starting from an integer you choose. |
| **4** | Vanity search for a **Hash160 integer prefix** (parallel). |
| **5** | Vanity search for an **address prefix** (Base58, P2PKH). |
| **6** | Exact address search – stops after the first hit. |
| **7** | Build and query a Bloom filter from `FullKeyPairs.csv`. |
| **8** | Vanity search for both **prefix & suffix** on the address. |
| **9** | Combo vanity: **WIF prefix + address prefix** must both match. |

## Installation

```bash
python -m venv venv
source venv/bin/activate          # or .\venv\Scripts\activate on Windows
pip install -r requirements.txt   # see below

# Key-SiteFinder (English UI)

A tiny helper that tells you **which page** a given Bitcoin private key would
appear on in a page-by-page key listing (120 entries per page) and prints every
derived value (WIF, address, Hash160, etc.).

This file is simply the English translation of the original German script.
No cryptographic logic changed.

---

## Quick Start

```bash
python key_sitefinder_en.py
