# Assignment


The project includes:

✔ Overview
✔ Features
✔ Folder structure
✔ Dependencies
✔ Installation steps
✔ How to run
✔ Troubleshooting
✔ Notes about PDFs, regex, and model-free extraction

# **PDF Data Extraction → Expected Output Excel**

This project automates the extraction of structured information from a narrative-style PDF and exports it into an Excel file that matches the format of **Output.xlsx**.

The script reads the PDF:

```
Data Input.pdf
```

and generates an Excel file:

```
Output.xlsx
```

with a single sheet named **Output**, containing the following columns:

```
# | Key | Value | Comments
```

---

# ⭐ **Features**

### ✔ Extracts all major categories:

* **Personal Information**
* **Education (High School, B.Tech, M.Tech)**
* **Work Experience (multiple companies)**
* **Certifications (AWS, Azure, PMP, SAFe, etc.)**
* **Skills with ratings**
* **Salary information**
* **Context sentences**
* **Other unmatched sentences** (ensures 100% content capture)

### ✔ Structured Parsing

Uses pattern-based extraction through regex and sentence-matching logic.

### ✔ Comments Field

Every extracted value includes the **original sentence** from the PDF for traceability.

### ✔ Matching Expected Output Format

The structure and sheet name exactly match our provided **Output.xlsx** template.

### ✔ Beginner-Friendly but Full-Featured

The code is cleaned and reorganized (Option B), maintaining full extraction power.

---

# 📂 **Project Structure**

```
project/
│
├── Data Input.pdf
├── Output.xlsx            (Generated automatically)
├── Assinment.ipynb        (Your main Python script)
└── README.md
```

---

# 🔧 **Dependencies**

Install the following Python packages:

```
pdfplumber
pandas
openpyxl
```

To install all at once:

```bash
pip install pdfplumber pandas openpyxl
```

---

# 🚀 **Usage Instructions**

## **1. Place the Input File**

Ensure the PDF is available at:

```
C:/Users/Acer/New-Python_dir/assisment/Data Input.pdf
```

OR modify:

```python
PDF_PATH = "path/to/Data Input.pdf"
```

## **2. Run the Assignment Script in jupyter notebook**

Assignment.ipynb

## **3. Output File**

The script will produce:

```
C:/Users/Acer/New-Python_dir/assisment/Output.xlsx
```

We will see a message like:

```
Written 30 rows to Output.xlsx
```

---

# 🧠 **How It Works (Simplified)**

1. **pdfplumber** extracts all text from the PDF
2. The text is split into sentences
3. Specialized extractors scan for:

   * Names, DOB, Birthplace
   * Education milestones
   * Career timeline
   * Certification achievements
   * Skill ratings
4. Each extracted item is stored as:

   ```
   (Key, Value, Comments)
   ```
5. Items are numbered and exported to Excel

---

# 🛑 Troubleshooting

### **PDF text not extracted**

Make sure **text is selectable** in our PDF (not scanned).
If it's a scanned PDF → we must use OCR (Tesseract).

### **Regex not matching**

our resume or document must follow a similar structure
because extraction depends on predictable patterns.

### **Output Excel not updating**

Close the file before running the script again.

---

# 📌 Notes

* No ML models are used — the extraction relies only on **regex** and **rule-based NLP**.
* The script is optimized for the structure of **Data Input.pdf**.
* We can extend extraction logic easily by adding new regex patterns.

