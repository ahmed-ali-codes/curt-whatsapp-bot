# 📘 CURT — Curtin University AI Study Assistant

> An AI-powered study tool that transforms your lecture materials into questions, quizzes, and summaries using Google Gemini.

![Python](https://img.shields.io/badge/Python-3.10%2B-3776AB?logo=python&logoColor=white)
![Gemini](https://img.shields.io/badge/Google%20Gemini-2.5%20Flash-4285F4?logo=google&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

---

## 🎯 What is CURT?

**CURT** is a command-line study assistant built for Curtin University students. Drop in your lecture slides, notes, or documents — and CURT uses **Google Gemini AI** to instantly generate:

- ✅ **Short Q&A** — 10 question-and-answer pairs for quick revision
- ✅ **Multiple Choice Questions** — 10 MCQs with 4 options each
- ✅ **Concise Summaries** — Key points distilled from your material

No more manually writing flashcards or skimming 80-page PDFs before exams. Let AI do the heavy lifting.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| **Python 3.10+** | Core language |
| **Google Gemini 2.5 Flash** | AI content generation |
| **PyMuPDF (fitz)** | PDF text extraction |
| **python-docx** | Word (.docx) text extraction |
| **python-pptx** | PowerPoint (.pptx) text extraction |
| **python-dotenv** | Secure environment variable management |

---

## 📂 Project Structure

```
curt-whatsapp-bot/
├── curt.py            # Main application
├── .env               # Your API key (git-ignored)
├── .env.example       # Template for collaborators
├── .gitignore         # Git ignore rules
├── README.md          # You are here
└── output_*.txt       # Generated outputs (git-ignored)
```

---

## 🚀 Getting Started

### Prerequisites

- Python 3.10 or higher
- A [Google Gemini API key](https://aistudio.google.com/app/apikey)

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR_USERNAME/curt-whatsapp-bot.git
cd curt-whatsapp-bot
```

### 2. Install Dependencies

```bash
pip install google-generativeai pymupdf python-docx python-pptx python-dotenv
```

### 3. Set Up Your API Key

Copy the example environment file and add your Gemini API key:

```bash
cp .env.example .env
```

Then edit `.env`:

```env
GEMINI_API_KEY=your_actual_api_key_here
```

> ⚠️ **Never commit your `.env` file.** It's already in `.gitignore`.

### 4. Run CURT

```bash
python curt.py
```

---

## 💡 Usage

Once running, you'll see an interactive menu:

```
=== 📘 Study Material Assistant (PDF, Word, PPT → Gemini AI) ===

Select a task:
1️⃣  Generate Short Questions & Answers
2️⃣  Generate MCQs (Multiple Choice Questions)
3️⃣  Summarize the File
4️⃣  Exit

👉 Enter your choice (1/2/3/4):
```

1. **Pick a task** (1, 2, or 3)
2. **Provide the file path** to your PDF, Word, or PowerPoint file
3. **Get AI-generated output** printed to the console and saved to a file

### Output Files

| Task | Output File |
|---|---|
| Short Q&A | `output_shortqa.txt` |
| MCQs | `output_mcqs.txt` |
| Summary | `output_summary.txt` |

---

## 📋 Supported File Formats

| Format | Extension | Library Used |
|---|---|---|
| PDF | `.pdf` | PyMuPDF |
| Microsoft Word | `.docx` | python-docx |
| Microsoft PowerPoint | `.pptx` | python-pptx |

---

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📝 License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgements

- [Google Gemini AI](https://ai.google.dev/) — for powering the content generation
- [Curtin University](https://www.curtin.edu.au/) — inspiration for the project
- Built during the **Curtin University Hackathon 2026** 🏆
