# 🤖 AI Agents & LLM Applications

A hands-on AI engineering project focused on learning how **LLMs, AI Agents, Tool Calling, RAG, Vector Databases, Agent Memory, Multimodal AI, Guardrails, and LLM Evaluation** work together.

I built these projects for learning purposes, starting with basic LLM calls and gradually moving toward more complete AI applications. The main goal was to understand not only how to use AI frameworks, but also what happens behind the scenes when an agent calls tools, retrieves information, maintains memory, processes images, protects sensitive data, and evaluates its own responses.

## 📦 Technologies

- `Python`
- `LangChain`
- `LangGraph`
- `Groq`
- `Google Generative AI`
- `Chroma`
- `Hugging Face Embeddings`
- `Sentence Transformers`
- `LangSmith`
- `Streamlit`
- `Pandas`
- `NumPy`
- `Scikit-learn`
- `PyPDF`
- `Jupyter Notebook`
- `python-dotenv`

## 🦄 Features

Here's what I explored and built in this project:

- **LLM Applications**: Worked with LLM APIs, prompts, system/user messages, temperature, and different model providers.

- **AI Agents**: Built agents that can understand a user's request and decide when to use available tools.

- **Tool Calling**: Created Python functions as tools and explored how agents generate tool names and arguments based on natural-language requests.

- **Product Query Agent**: Built a product assistant that can retrieve product information such as price, rating, description, and reviews using multiple tools.

- **Agent Memory**: Added conversation memory using `InMemorySaver` and `thread_id` to maintain state across interactions.

- **Inventory Agent**: Built an inventory assistant that uses a dedicated inventory tool to retrieve product stock information instead of guessing.

- **Vector Databases**: Used Chroma and embeddings to store documents and perform semantic similarity searches.

- **RAG**: Built a Retrieval-Augmented Generation pipeline using PDF documents, text splitting, embeddings, Chroma, retrieval, prompts, and LLM generation.

- **Multimodal AI**: Built a blood work analysis workflow using a vision-capable model to analyze images, extract test results, identify abnormal values, and use tool calling for diet recommendations.

- **Guardrails**: Used `PIIMiddleware` to explore protecting sensitive information such as credit card numbers and email addresses through masking and redaction.

- **LLM Evaluation**: Built LangSmith evaluation workflows to compare expected and actual responses.

- **Tool-Call Evaluation**: Evaluated whether an agent selected the correct tool and passed the expected arguments.

- **Semantic Similarity**: Used `all-MiniLM-L6-v2` embeddings and cosine similarity to compare the meaning of text rather than relying only on exact string matching.

- **LLM-as-a-Judge**: Used a separate LLM to evaluate response quality based on relevance, correctness, and format compliance.

- **Streamlit Application**: Built a Blood Work Analyzer application with a two-stage LLM workflow for extraction and health-summary generation.

## 👩🏽‍💻 The Process

I started by learning the basics of calling LLMs from Python. I worked with prompts, system and user messages, model configuration, and temperature to understand how an LLM receives information and generates a response.

Once I understood basic LLM calls, I moved into **tool calling**.

I created Python functions and exposed them as tools to an agent. This helped me understand the difference between a simple LLM application and an agent that can interact with external functions.

Next, I built a **Product Query Agent**. The agent could retrieve product information and later use a separate review tool. This helped me understand how an agent can select between multiple tools depending on the user's request.

After that, I explored **agent memory** using `InMemorySaver` and `thread_id`. This helped me understand how an agent can maintain state across different interactions and how separate conversations can be identified.

I then built an **Inventory Agent** that uses a dedicated inventory tool. The agent was instructed to retrieve inventory information from the tool rather than making assumptions or guessing.

The next step was learning about **embeddings and vector databases**.

I used Chroma to store documents and experimented with semantic search. This helped me understand how text can be converted into vectors and how similarity search can retrieve information based on meaning.

From there, I built a complete **RAG pipeline**.

The workflow loads a PDF, splits the document into chunks, creates embeddings, stores them in Chroma, retrieves relevant documents, and passes the retrieved context to an LLM.

After understanding RAG, I explored **Multimodal AI**.

I worked with a vision-capable model that receives a blood work image along with instructions. The model extracts test results, identifies values outside the normal range, and works with a tool-based workflow to provide diet recommendations.

I then explored **Guardrails and PII protection**.

Using `PIIMiddleware`, I experimented with masking credit card information and redacting email addresses. This helped me understand how privacy and security controls can be added around an AI workflow.

Finally, I focused on **LLM Evaluation**.

I created LangSmith datasets and evaluators to compare expected and actual outputs. I explored semantic similarity using embeddings and cosine similarity, evaluated individual tool calls, and built an LLM-as-a-Judge workflow to evaluate relevance, correctness, and format compliance.

## 📚 What I Learned

### 🧠 LLMs & Prompting

- How to call LLMs from Python.
- How system and user messages work.
- How prompts influence model behavior.
- How temperature affects model output.
- How different LLM providers can be integrated into applications.

### 🤖 AI Agents

- How agents differ from basic LLM calls.
- How agents decide when to use tools.
- How tool arguments are generated.
- How multiple tools can be connected to one agent.
- Why agents should use tools for factual information instead of guessing.

### 🛠️ Tool Calling

- How to create Python functions as tools.
- How tool inputs and arguments are structured.
- How an agent decides which tool to call.
- How to inspect tool calls after an agent execution.
- How tool selection and arguments can be evaluated.

### 🧠 Agent Memory

- How conversation state works.
- How `InMemorySaver` stores agent state.
- How `thread_id` identifies different conversations.
- The difference between stateless and stateful agents.

### 🔎 Embeddings & Vector Databases

- How text is converted into numerical embeddings.
- How semantic similarity works.
- How Chroma stores and retrieves vectors.
- How semantic search differs from keyword-based search.

### 📄 Retrieval-Augmented Generation

- Document loading.
- Text splitting.
- Chunk size and overlap.
- Embedding generation.
- Vector storage.
- Retrieval.
- Prompt construction.
- Passing retrieved context to an LLM.

The overall RAG workflow:

```text
PDF
 ↓
Document Loader
 ↓
Text Splitter
 ↓
Embeddings
 ↓
Chroma
 ↓
Retriever
 ↓
Relevant Context
 ↓
Prompt
 ↓
LLM
 ↓
Final Answer
