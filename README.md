### An AI-powered Career \& Document Analyzer 🚀



The idea started from a simple problem:

Most people send CVs, portfolios, project descriptions, or technical profiles without really knowing:

how well they match a job,

what skills are missing,

or why they keep getting rejected.



So we built a system that analyzes professional/job-related documents and turns them into actionable insights.



##### 🔍 What the platform does



Upload a CV or any career-related document , the Number of top matching job roles and the system can:



✅ Extract and analyze content automatically

✅ Detect skills, technologies, and tools (requirements)

✅ Match the document against relevant job profiles

✅ Generate an overall compatibility score

✅ Identify missing requirements and weak areas

✅ Recommend important technologies/tools to add

✅ Provide a practical improvement roadmap

✅ Support multilingual documents through language normalization



##### 🧠 Built with



Backend (Python 🐍) : FastAPI, NLP pipelines, Sentence Transformers, semantic similarity models, and a custom ML-based scoring system



Frontend: HTML, CSS, and JavaScript



⚙️ Infrastructure \& technical stack



We used CPU-optimized PyTorch and TorchVision to keep inference lightweight and requests as fast as possible.



The platform also supports multilingual normalization with LangDetect and Deep Translator, document parsing with PDFPlumber and Python-Docx, and fuzzy skill matching with RapidFuzz.



Deployed on Railway, with GitHub used for collaboration, maintenance, and continuous development.



Our goal was to build something more useful than a basic CV checker — a tool that gives practical insights people can actually use to improve their opportunities.



Still improving it every day, and we’d love to hear feedback from the community 



the link 👇

🔗 [https://lnkd.in/eF2RKHCc](https://lnkd.in/eF2RKHCc)



#### CV Analyzer — Frontend

A sleek, dark-themed frontend for the CV Analyzer API.
No build tools required — pure HTML, CSS, JavaScript.

\---

#### 📁 Project Structure

```
cv-analyzer-frontend/
├── index.html          ← Main page (upload + results)
├── css/
│   └── style.css       ← All styles (dark editorial theme)
├── js/
│   └── app.js          ← API integration + rendering logic
└── README.md
```

\---

### 🚀 How to Run

#### 1\. Start the Backend API

Make sure your FastAPI server is running locally:

```bash
# Install dependencies
pip install -r requirements.txt

# Start the server
uvicorn cv\_api:app --reload --port 8000
```

The API must be accessible at: `http://localhost:8000`

#### 2\. Open the Frontend

Simply open `index.html` in your browser:

```bash
# Option A: double-click index.html in your file manager

# Option B: use a simple local server (recommended, avoids CORS issues)
python -m http.server 3000
# then open http://localhost:3000
```

> \*\*Recommended:\*\* Use a local server (VS Code Live Server, Python's http.server, etc.)  
> Opening `index.html` directly via `file://` may cause CORS issues in some browsers.

\---

#### 🔧 Configuration

The API base URL is set at the top of `js/app.js`:

```js
const API\_BASE = 'http://localhost:8000';
```

Change this if your API runs on a different port or host.

\---

#### 📤 Input

|Field|Description|Default|
|-|-|-|
|**CV File**|PDF, DOCX, DOC, or TXT|—|
|**Top K**|Number of job matches to retrieve (1–20)|5|
|**Threshold**|Minimum similarity score (0.10–0.90)|0.30|

\---

#### 📊 Output Sections

|Section|Description|
|-|-|
|**Best Job**|Top matching job title, similarity, description|
|**Match Score**|Overall score /100, /10, match level badge|
|**Score Breakdown**|Requirements score, Tools score, Semantic similarity|
|**Detected Jobs**|All matched jobs with similarity bars|
|**Summary**|Short explanation of results|
|**Top Strengths**|Skills found in CV with evidence|
|**Priority Improvements**|Missing skills with how-to advice|
|**Technologies Found**|Tech chips extracted from CV|
|**Recommended Tools**|Tools to learn, ranked by relevance|
|**Action Plan**|Prioritized steps (High / Medium / Low)|
|**Language**|Detected CV language + translation status|

\---

#### 🎨 Design

* **Theme:** Dark editorial / brutalist-refined
* **Fonts:** Syne (display) + DM Mono (body) + Instrument Serif (accents)
* **Colors:** Deep dark bg + violet accent + semantic color coding
* **Animations:** Gauge counter, fade-in cards, loading ring

