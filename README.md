# ◰ supabasePipeline

**Convert any CSV to Supabase-ready SQL – instantly, in your browser.**

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Vercel](https://img.shields.io/badge/Deployed%20on-Vercel-black)](https://supabasepipeline.vercel.app/)

> No uploads. No servers. Your data stays local.

---

## 🔧 What it does

`supabasePipeline` is a 100% client-side tool that helps you turn messy CSV files into clean SQL for Supabase. It automatically detects column types, lets you visually map (and merge) columns, and generates both `CREATE TABLE` and `INSERT` statements – all without ever sending your data to a server.

---

## ✨ Features

- **Drag & drop mapping** – drag CSV columns onto Supabase columns
- **Auto‑type detection** – infers integers, dates, booleans, and text
- **Merge columns** – combine multiple CSV columns into one (e.g., `first_name` + `last_name` → `full_name`)
- **Auto‑delimiter detection** – when merging, it picks the right separator (space, comma, hyphen, etc.)
- **Rename target columns** – double‑click or use the ✎ button
- **Fetch existing schema** – connect to Supabase (read‑only) to match your existing table
- **Generate SQL** – `CREATE TABLE` and `INSERT` statements with one click
- **Push directly** – insert data into Supabase via the API (requires insert permission)
- **Auto‑map toggle** – turn automatic mapping on/off

---

## 🚀 Live Demo

Try it now: [supabasepipeline.vercel.app](https://supabasepipeline.vercel.app/)

---

## 📖 How to use

### 1. Upload your CSV
Click the file input or drag a `.csv` file into the upload area. The tool will parse the headers and sample rows to infer column types.

### 2. (Optional) Fetch your Supabase schema
Enter your Supabase URL, anon key, and table name, then click **Fetch**. This will pull the existing column names and data types so you can map your CSV to an existing table.

### 3. Map columns
- **Drag** a source column (green chip) and drop it onto a target column (purple/blue chip).
- **Click** a source column, then click a target column (alternative).
- **Merge** multiple sources into one target: drag a second source onto an already‑mapped target – the tool will automatically detect a delimiter and merge them.

### 4. Generate SQL or push
- **CREATE** – generates the full `CREATE TABLE IF NOT EXISTS` SQL. Copy it and run in Supabase SQL Editor.
- **INSERT** – generates the `INSERT INTO ... VALUES` statements.
- **PUSH** – directly inserts the data into Supabase via the REST API (requires insert permission and a key with proper RLS).

---

## 🔒 Privacy & Security

- All processing happens **client‑side** – your CSV, Supabase keys, and data are **never sent** to any third‑party server.
- The Supabase API calls are made directly from your browser, using the credentials you provide.

---

## 🧩 Technical Stack

- Vanilla JavaScript (ES6)
- Tailwind CSS (via CDN)
- Papa Parse – CSV parsing
- Supabase JS SDK – schema fetching and data insertion

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.

---
