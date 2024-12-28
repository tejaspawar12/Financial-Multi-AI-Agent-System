# Financial Multi-AI System

This repository contains a **Financial Multi-AI System**, a project designed to harness the power of multiple AI agents to provide financial insights and web search capabilities. Built using cutting-edge tools and APIs, the system integrates functionalities like financial data retrieval, stock analysis, and web searches, making it a versatile tool for financial analysis and decision-making.

---

## Features

- **Web Search Agent**: Uses DuckDuckGo to fetch web information with source citations.
- **Financial AI Agent**: Retrieves real-time financial data, including:
  - Stock prices
  - Analyst recommendations
  - Stock fundamentals
  - Latest company news
- **Multi-AI Team**: Combines the capabilities of multiple agents to handle complex queries efficiently.
- **Streamlined Responses**: Outputs data in markdown format, including tables for structured financial data.

---

## Tech Stack

### Python Libraries
- **[phidata](https://github.com/phidatahq/phidata)**: Core library for building AI agents.
- **python-dotenv**: Manages environment variables securely.
- **yfinance**: Fetches financial data from Yahoo Finance.
- **packaging**: For version handling and compatibility.
- **duckduckgo-search**: Performs web searches using DuckDuckGo.
- **fastapi**: Web framework for building APIs.
- **uvicorn**: ASGI server for running the FastAPI app.
- **groq**: Integrates advanced AI models.
- **openai**: Accesses OpenAI's GPT models.

---

## Installation

### Prerequisites
- Python 3.8 or higher
- An OpenAI API key

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/financial-multi-ai-system.git
   cd financial-multi-ai-system
   ```
2. Create a virtual environment and activate it:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Set up environment variables:
   - Create a `.env` file in the root directory:
     ```env
     OPENAI_API_KEY=your_openai_api_key
     ```

---

## Usage

### Running the System
1. Start the FastAPI server:
   ```bash
   uvicorn main:app --reload
   ```
2. Interact with the agents via the FastAPI interface at `http://127.0.0.1:8000/docs`.

### Example Query
- **Input**: "Summarize analyst recommendations and share the latest news for NVDA."
- **Output**:
  - Analyst recommendations in a tabular format.
  - Latest news articles with sources cited.

---

## Project Structure
```
financial-multi-ai-system/
├── main.py                # Entry point for the FastAPI app
├── agents/
│   ├── web_search_agent.py  # Web search agent implementation
│   ├── finance_agent.py     # Financial agent implementation
│   └── multi_ai_agent.py    # Multi-agent team
├── tools/
│   ├── yfinance_tools.py    # Tools for financial data
│   └── duckduckgo_tools.py  # Tools for web search
├── requirements.txt       # Python dependencies
├── .env.example           # Example environment variables
└── README.md              # Project documentation
```

---

## Contributing

Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature:
   ```bash
   git checkout -b feature-name
   ```
3. Commit your changes and push them to your fork:
   ```bash
   git commit -m "Add feature-name"
   git push origin feature-name
   ```
4. Submit a pull request.

---

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments

- **OpenAI** for GPT models.
- **Yahoo Finance** for financial data.
- **DuckDuckGo** for web search capabilities.

---

## Contact

For questions or support, feel free to reach out via [your email/contact info].
