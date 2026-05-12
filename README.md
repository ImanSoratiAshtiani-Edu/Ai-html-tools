# 🐍 Python & ML Mastery Course

> A comprehensive, self-paced Python and Machine Learning learning platform — built for serious learners aiming for long-term mastery.

[![Python](https://img.shields.io/badge/Python-3.11+-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)](https://streamlit.io/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Lessons](https://img.shields.io/badge/Lessons-104-blueviolet)](#-curriculum)
[![Phases](https://img.shields.io/badge/Phases-15-success)](#-curriculum)

---

## 📖 About

This is a complete Python and Machine Learning curriculum delivered as a static, file-based learning platform. **No build step, no server required** — just open `index.html` in any browser.

Each lesson combines conceptual explanations, multiple code examples, performance considerations, and hands-on exercises with reference solutions. Content is written primarily in **Persian (Farsi)** with English code and technical terms — designed for Persian-speaking learners working with English-language tooling.

### Why this exists

Most online courses optimize for engagement (short videos, quick wins). This platform optimizes for **deep understanding** — proper internals, performance trade-offs, production patterns, and the *why* behind every decision.

---

## ✨ Features

- 📚 **104 lessons** across 15 phases — from Python fundamentals to ML pipelines in production
- 🎯 **Modular architecture** — each lesson is a single JS file; loaded dynamically
- 🌓 **Light & dark themes** with auto system detection
- ⚙️ **Customizable** — fonts, sizes, colors, and syntax highlighting in-app
- 🔍 **Searchable** across all lessons
- ⌨️ **Keyboard shortcuts** for navigation (J/K, prev/next)
- 🐍 **In-browser Python execution** via [Pyodide](https://pyodide.org/) — run examples without leaving the page
- 📱 **Responsive** — works on desktop, tablet, and mobile
- 🌐 **RTL-aware** — handles mixed Persian/English content correctly
- 💾 **Zero dependencies** — pure HTML/CSS/JavaScript, runs on `file://` protocol

---

## 🎓 Curriculum

15 phases, 104 lessons, ~50 hours of focused content.

| Phase | Topic | Lessons | Status |
|-------|-------|---------|--------|
| **0** | Foundations (types, control flow, functions, errors, modules) | 10 | ✅ |
| **1** | Data Structures (list, dict, set, deque, heap, ABCs) | 8 | ✅ |
| **2** | OOP (inheritance, dataclasses, descriptors, metaclasses) | 6 | ✅ |
| **3** | NumPy (arrays, broadcasting, indexing, performance) | 7 | ✅ |
| **4** | Pandas (Series, DataFrame, groupby, merge, time series) | 15 | ✅ |
| **5** | Visualization (Matplotlib, Seaborn, Plotly) | 4 | ✅ |
| **6** | Statistics (descriptive, distributions, tests, regression) | 4 | ✅ |
| **7** | ML Foundations (sklearn, models, evaluation, tuning) | 9 | ✅ |
| **8** | Unsupervised Learning (clustering, PCA, t-SNE) | 4 | ✅ |
| **9** | Tooling (Git, pytest, uv/ruff/mypy, logging, Docker) | 5 | ✅ |
| **10** | Web & Concurrency (HTTP, async, threading, FastAPI) | 6 | 🚧 |
| **11** | Text Mining (regex, NLP basics, embeddings) | 6 | ✅ |
| **12** | Database Mastery (SQL, SQLAlchemy, migrations) | 8 | ✅ |
| **13** | Streamlit (widgets, layouts, caching, deployment) | 6 | ✅ |
| **14** | ML Pipeline End-to-End (architecture → capstone) | 6 | ✅ |

### Highlighted lessons

- **MLP5 — Capstone** — Full Streamlit ML app integrating preprocessing pipeline, model serving, and UX best practices
- **NP7** — NumPy performance: memory layout, contiguity, vectorization
- **PD7** — Pandas `groupby` with `agg`, `transform`, multi-level operations
- **OOP6** — Descriptors, metaclasses, and the Python data model
- **MLP6** — Production MLOps: MLflow tracking, drift detection, CI/CD

---

## 🚀 Quick Start

### Option 1: Open locally (recommended)

```bash
git clone https://github.com/YOUR_USERNAME/python-ml-course.git
cd python-ml-course
# Open in browser
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

That's it. No installation, no build step.

### Option 2: Serve with Python (optional)

```bash
python -m http.server 8000
# Open http://localhost:8000
```

### Option 3: GitHub Pages

Fork this repo, enable GitHub Pages on the `main` branch, and access at:
`https://YOUR_USERNAME.github.io/python-ml-course/`

---

## 📁 Project Structure

```
python-ml-course/
├── index.html                  # Single entry point
├── README.md
├── LICENSE
│
├── assets/
│   ├── style.css               # Slate v2 palette, WCAG AA/AAA
│   ├── core.js                 # Sidebar, navigation, dynamic loading
│   ├── settings.js             # In-app settings panel
│   └── pyodide-runner.js       # In-browser Python execution
│
├── lessons-index.js            # Metadata for all 104 lessons
│
└── lessons/                    # One file per lesson
    ├── F1.js                   # Phase 0 — Foundations
    ├── F2.js
    ├── ...
    ├── DS1.js                  # Phase 1 — Data Structures
    ├── ...
    ├── MLP5.js                 # Phase 14 — Capstone
    └── MLP6.js
```

### Lesson structure

Each lesson is a JavaScript file exporting a single object:

```javascript
window.LESSONS['ID'] = {
  id: 'F1',
  title: 'Python Types and Variables',
  lead: 'Brief introduction...',
  duration: '~25 min',
  prereq: 'None',
  packages: 'Python core',
  
  concept: { /* high-level intro */ },
  sections: [ /* explanation + examples + exercises */ ],
  cheatsheet: [ /* key takeaways */ ],
  references: [ /* source materials */ ],
};
```

---

## 🛠️ Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — no framework, no build tools
- **[Pyodide](https://pyodide.org/)** — Python runtime in WebAssembly (for code execution)
- **[Prism.js](https://prismjs.com/)** — syntax highlighting
- **B Lotus** (Persian) + **JetBrains Mono** (code) — typography

---

## 🎨 Customization

The settings panel (gear icon) provides full control over:

- **Fonts** — Persian, English, and monospace independently
- **Sizes** — base font, code, headings, line height
- **Colors** — background, foreground, accents, code theme
- **Syntax themes** — multiple Prism themes available

All preferences are persisted in `localStorage`.

---

## 📸 Screenshots

> _Add screenshots here once deployed — recommended: home page, lesson view, settings panel, code execution, dark mode_

```
[screenshot: lesson view with code blocks]
[screenshot: settings panel]
[screenshot: mobile responsive view]
```

---

## 🤝 Contributing

Contributions are welcome! Here are good entry points:

- **Fix typos or improve clarity** in existing lessons (`lessons/*.js`)
- **Add exercises** with reference solutions
- **Improve translations** (Persian → English or vice versa)
- **Suggest new lessons** for Phase 10 (Web & Concurrency) which is in progress

### How to contribute a lesson edit

1. Fork the repo
2. Edit the relevant `lessons/XX.js` file
3. Test by opening `index.html` locally
4. Submit a pull request with a clear description

### Style guide

- Persian explanations in `text`, `callout`, `list` blocks
- English code in `code` blocks
- Type hints required on all Python functions
- Mention performance/memory trade-offs where relevant
- Each exercise must have a reference solution with `solutionNote`

---

## 📚 Learning Path Recommendations

### Complete beginner
Start with **Phase 0** → **Phase 1** → **Phase 2** (OOP).
Estimated time: 30 hours.

### Data Scientist (focus on analysis)
**Phase 0** (skim) → **Phase 3** (NumPy) → **Phase 4** (Pandas) → **Phase 5** (Viz) → **Phase 6** (Stats).
Estimated time: 25 hours.

### ML Engineer (focus on production)
**Phase 0-2** (skim) → **Phase 7** (ML) → **Phase 9** (Tooling) → **Phase 12** (Database) → **Phase 13** (Streamlit) → **Phase 14** (ML Pipeline).
Estimated time: 35 hours.

### Specific topics
Each lesson is self-contained when prerequisites are met. Use the sidebar to jump directly.

---

## ⚠️ Disclaimer

This course is a **personal learning project**. While it's been built carefully, it:

- Is not a substitute for official documentation
- May contain errors or outdated information (Python and library APIs evolve)
- Reflects opinionated choices (modern tooling, type hints everywhere)

For authoritative information, always refer to official sources: [python.org](https://python.org), [scikit-learn.org](https://scikit-learn.org), etc.

---

## 📜 License

MIT — see [LICENSE](LICENSE) file.

You're free to use, modify, and distribute this content for personal or educational purposes.

---

## 🙏 Acknowledgments

- **[Python Software Foundation](https://www.python.org/psf/)** — for the language
- **[NumPy](https://numpy.org/)**, **[Pandas](https://pandas.pydata.org/)**, **[scikit-learn](https://scikit-learn.org/)** — for the tools
- **[Pyodide](https://pyodide.org/)** — for making in-browser Python possible
- **[Streamlit](https://streamlit.io/)** — for inspiration on accessible data apps
- All authors of the open-source libraries referenced throughout

---

## 📬 Contact

- **Author**: Iman Sorati Ashtiani
- **Location**: Bologna, Italy 🇮🇹
- **GitHub**: [@YOUR_USERNAME](https://github.com/YOUR_USERNAME)

If you find this useful, ⭐ star the repo!

---

<p align="center">
  Made with ☕ in Bologna · For learners who care about getting it right
</p>
