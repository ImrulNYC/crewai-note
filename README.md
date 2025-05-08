# 🧠 Agent-Note–Composition

## Description

**Agent-Note–Composition** is a Streamlit-based application that uses [CrewAI](https://github.com/joaomdmoura/crewai) agents to convert raw input into structured, easy-to-review notes. Users can input content via direct text, PDF, or DOCX file uploads.

---

## 🔄 Information Flow

1. If the input is a file, the app extracts text using `PyPDF2` or `docx2txt`.
2. The extracted or pasted content is passed to a crew of AI agents.
3. Each agent processes the input sequentially to prepare structured notes.

---

## 🧠 Agents

- **Grammar Agent**: Corrects grammar and resolves inconsistencies in the writing.
- **Fact-check Agent**: Validates factual accuracy using web search.
- **Format Agent**: Applies the selected note-taking method:
  - Outline Method  
  - Cornell Method  
  - Boxing Method  
- **(Optional) Flashcards Agent**: Generates 5 to 15 flashcards summarizing key concepts and facts.

---

## 🧰 Technologies

- **CrewAI** – Orchestrates a team of AI agents  
- **Streamlit** – Interactive UI and Markdown rendering  
- **PyPDF2** – Extracts text from PDF files  
- **docx2txt** – Extracts text from Word documents  
- **LiteLLM** – Lightweight interface to call LLMs  
- **python-dotenv** – Manages environment variables securely  

---

## 🚀 Installation

### 1. Prerequisites

- Python `>=3.10` and `<3.13`
- [`uv`](https://github.com/astral-sh/uv) for environment and dependency management

### 2. Install `uv`

```bash
pip install uv
```

###3. Clone the Repository
git clone https://github.com/Rigo-stack/crewai-note.git
cd crewai-note
###4. Install Dependencies
uv pip install -r requirements.txt
###5. Set Up Environment Variables
Create a .env file or export the following variables:

```OPENAI_API_KEY=your_openai_key
SERPER_API_KEY=your_serper_key
```
### 6. Launch the App
streamlit run app.py
⚙️ Usage & Customization


agents.yaml: Define the agents and their roles
tasks.yaml: Configure the task sequence
crew.py: Add tools, logic, and specific task parameters
app.py: Modify input fields and Streamlit interactions

