# SupabasePipeline · CSV to SQL Converter & Schema Editor

SupabasePipeline is a lightweight, client-side tool that instantly converts any CSV file into ready-to-run SQL for [Supabase](https://supabase.com). It auto-detects column types, lets you edit schema on the fly, and generates `CREATE TABLE` + sample `INSERT` statements — all in your browser. No uploads, no server, no tracking.


## Features

- **Drag & drop CSV import** – instantly loads your data
- **Smart type inference** – automatically detects `TEXT`, `INTEGER`, `FLOAT`, `BOOLEAN`, or `TIMESTAMP`
- **Interactive schema editor** – rename columns, change types, set nullable, toggle primary keys
- **Live SQL preview** – updates as you edit, copy with one click
- **Data preview** – see the first 120 rows, edit cell values, toggle a sample row
- **Works 100% offline** – runs entirely in your browser (no server, no API)
- **Lightweight & fast** – single HTML file, no dependencies besides Papa Parse (loaded from CDN)

## Live Demo

Try it now: [https://supabasepipeline.vercel.app](https://supabasepipeline.vercel.app)

## How to use

1. **Upload your CSV**  
   Drag a CSV file onto the drop zone or click to browse. The file must have headers in the first row.

2. **Review & adjust the schema**  
   - Click any column name to rename it.  
   - Click the **⋮** (kebab) menu to change data type, set nullable, or toggle primary key.  
   - Edit any cell directly in the table to fix values.  
   - Click **⟳ infer types** to re‑analyze types from the full dataset.

3. **Generate SQL**  
   The SQL panel updates live. You can:  
   - Change the table name (top left).  
   - Click **copy sql** to copy the entire `CREATE TABLE` + sample `INSERT` statements.  

4. **Deploy to Supabase**  
   After copying, a handy guide appears with a link to the Supabase SQL Editor. Paste your SQL and run it.

## Local development

Because it's a single HTML file, you can run it anywhere:

```bash
# Clone the repository
git clone https://github.com/supabasepipeline/csv-to-sql.git

# Open the file directly in your browser
open supabasePipeline/index.html
