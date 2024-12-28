# Financial Multi-AI System

This repository contains a Financial Multi-AI System that leverages the power of Groq models, OpenAI, and various tools to provide advanced financial analysis and web search capabilities. The system is built using Python and includes two main components: `agent.py` and `playground.py`. Below is a detailed explanation of the project, its components, and how to set it up.

---

## Features

- **Multi-Agent Architecture**: Combines multiple AI agents to perform financial analysis and web searches.
- **Integration with Groq Models**: Utilizes Groq's advanced AI models for high-performance computation.
- **Financial Analysis Tools**: Provides stock prices, analyst recommendations, stock fundamentals, and company news using YFinanceTools.
- **Web Search Capabilities**: Searches the web for information using DuckDuckGo tools.
- **Interactive Playground**: Includes a web-based playground for interacting with the agents.
- **Environment Configuration**: Supports `.env` files for secure API key management.

---

## Project Structure

### `agent.py`

This file defines the core AI agents used in the project:

#### 1. **Web Search Agent**

- **Purpose**: Searches the web for information.
- **Model**: Groq model (`llama3-groq-70b-8192-tool-use-preview`).
- **Tools**: DuckDuckGo for web search.
- **Instructions**: Ensures sources are always included in the responses.
- **Features**:
  - Displays tool calls.
  - Outputs responses in Markdown format.

#### 2. **Finance AI Agent**

- **Purpose**: Provides financial analysis.
- **Model**: Groq model (`llama3-groq-70b-8192-tool-use-preview`).
- **Tools**: YFinanceTools for:
  - Stock prices.
  - Analyst recommendations.
  - Stock fundamentals.
  - Company news.
- **Instructions**: Uses tables to display financial data.
- **Features**:
  - Displays tool calls.
  - Outputs responses in Markdown format.

#### 3. **Multi-AI Agent**

- **Purpose**: Combines the Web Search Agent and Finance AI Agent into a single agent.
- **Model**: Groq model (`llama-3.1-70b-versatile`).
- **Instructions**: 
  - Always include sources.
  - Use tables to display data.
- **Functionality**: Executes tasks such as summarizing analyst recommendations and sharing the latest news for specific stocks (e.g., NVDA).

### `playground.py`

This file defines an interactive playground for users to interact with the agents via a web interface:

#### 1. **Web Search Agent**

- Same as defined in `agent.py`.

#### 2. **Finance AI Agent**

- Same as defined in `agent.py`.

#### 3. **Playground Setup**

- **Library**: Uses the `phi.playground` module to create an interactive web application.
- **Functionality**: Allows users to:
  - Query the agents.
  - Receive responses in a user-friendly web interface.
- **Execution**: Runs a FastAPI server using `uvicorn`.

---

## Installation

### Prerequisites

- Python 3.8+
- Anaconda or virtual environment (recommended)
- API keys for OpenAI and Groq.

### Clone the Repository

```bash
git clone https://github.com/yourusername/financial-multi-ai-system.git
cd financial-multi-ai-system
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Set Up Environment Variables

Create a `.env` file in the root directory and add the following:

```env
OPENAI_API_KEY=your_openai_api_key
PHI_API_KEY=your_phi_api_key
```

---

## Usage

### Running the Agents

1. **Agent Execution**:

   Run the `agent.py` file to execute the Multi-AI Agent:

   ```bash
   python agent.py
   ```

   Example query:

   ```
   Summarize analyst recommendation and share the latest news for NVDA.
   ```

2. **Interactive Playground**:

   Run the `playground.py` file to start the interactive web application:

   ```bash
   python playground.py
   ```

   Access the application at `http://127.0.0.1:8000` in your browser.

---

## Key Technologies

- **[phi](https://github.com/phi-ai/phi)**: Framework for building multi-agent systems.
- **[python-dotenv](https://github.com/theskumar/python-dotenv)**: Manages environment variables.
- **[yfinance](https://github.com/ranaroussi/yfinance)**: Fetches financial data.
- **[duckduckgo-search](https://github.com/deedy5/duckduckgo-search)**: Performs web searches.
- **[fastapi](https://fastapi.tiangolo.com/)**: Framework for building APIs.
- **[uvicorn](https://www.uvicorn.org/)**: ASGI server for FastAPI.
- **[groq](https://groq.com/)**: Advanced AI model provider.

---

## Future Enhancements

- Add more financial tools for in-depth analysis.
- Extend the playground to support additional query types.
- Optimize the agents for faster response times.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments

- Thanks to the creators of phi, yfinance, and other libraries for their contributions.
- Special thanks to Groq and OpenAI for providing cutting-edge AI models.
