<p align="left">
  <img 
    src="https://github.com/mariusstoica21/Agentic_AI/blob/main/images/Cover.png"
  >
</p>

# Agentic AI - Seminar

This repository contains three Jupyter Notebooks introducing **CrewAI**, a Python framework for building AI agents and multi-agent systems.

The seminars include practical examples using Google Gemini, external tools, Retrieval-Augmented Generation (RAG), different agent execution strategies, agent memory, and semantic caching.

## Seminar 1 – Introduction to CrewAI

**File:** `Seminar_1.ipynb`

Introduces the fundamental concepts of CrewAI through practical examples:

- **LLM Integration:** Calling Google Gemini models and configuring generation parameters.
- **Knowledge Cutoff:** Understanding the limitations of LLM training knowledge.
- **External Tools:** Using `SerperDevTool` to retrieve up-to-date information from the Internet.
- **Retrieval-Augmented Generation (RAG):** Indexing course documents and retrieving relevant information using `RagTool`.
- **Agent Workflows:** Additional examples of sequential and hierarchical execution, reasoning, and planning.

## Seminar 2 – Multi-Agent Collaboration, Reasoning, and Planning

**File:** `Seminar_2.ipynb`

Explores more advanced CrewAI concepts through five examples:

1. **Sequential Execution:** Two agents collaborate using RAG and task context sharing.
2. **Hierarchical Execution with a Custom Manager:** A manager coordinates specialized agents to generate a micro-credential proposal.
3. **Hierarchical Execution with an Automatic Manager:** CrewAI automatically creates a manager to coordinate tasks and delegate work.
4. **Agent Reasoning:** An agent analyzes and plans its approach before executing a task.
5. **Crew-Level Planning:** A planning component prepares execution instructions for multiple agents and tasks.

## Seminar 3 – Agent Memory and Semantic Caching

**File:** `Seminar_3.ipynb`

Introduces memory management and caching in CrewAI through four practical examples:

1. **Short-Term Memory (STM):** An interactive university AI tutor stores conversation history in a Python list and uses it to answer follow-up questions.
2. **Automatic Long-Term Memory (LTM) Extraction:** A Memory Curator identifies, validates, and saves useful information from conversations to persistent JSON storage when a new session is started.
3. **Memory Classification and Storage:** CrewAI's native `Memory` API classifies and stores user-profile, episodic, semantic, and procedural memories using persistent vector storage and scoped retrieval.
4. **Keyword and Semantic Caching:** Sentence Transformer embeddings, cosine similarity, and Top-K retrieval identify reusable explanations, reducing unnecessary LLM calls when a cache hit occurs.

## Requirements

The examples use **Python**, **Jupyter Notebook**, **CrewAI**, **Google Gemini**, and **CrewAI Tools**. Seminar 3 also uses **Pydantic**, **Sentence Transformers**, and **NumPy**.

Install the main dependencies:

```bash
pip install crewai crewai-tools python-dotenv sentence-transformers pydantic numpy jupyter
```

Create a `.env` file containing your API keys:

```env
GEMINI_API_KEY=your_gemini_api_key
SERPER_API_KEY=your_serper_api_key
```

The RAG examples also require `AI_Course_Extended.txt` in the `files/` directory.

## Running the Examples

Start Jupyter Notebook:

```bash
jupyter notebook
```

Open `Seminar_1.ipynb`, `Seminar_2.ipynb`, or `Seminar_3.ipynb` and execute the cells in order.

**Note:** Some examples require Internet access and valid API keys. Do not commit your `.env` file to GitHub.
