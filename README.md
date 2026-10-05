# financial-agentic-rag
Production-grade, self-corrective Agentic RAG for SEC 10-K financial analysis with LangGraph, Hybrid Search, and Ragas eval
financial-agentic-rag/
├── README.md                      # Production portfolio README with badges & architecture
├── pyproject.toml                 # uv & pip build dependencies
├── run_demo.py                    # Standalone interactive CLI demonstration
├── benchmark_results.json         # Automated evaluation report
├── data/raw/                      # Realistic SEC 10-K extracts (NVIDIA & Apple FY24)
├── src/
│   ├── ingestion/                 # Table-preserving parser & contextual hierarchical chunker
│   ├── retrieval/                 # ChromaDB + BM25Plus + Reciprocal Rank Fusion + FlashRank
│   ├── agent/                     # Cyclical LangGraph state machine & verification graders
│   ├── evaluation/                # Golden Q&A dataset & benchmark runner
│   └── ui/app.py                  # Streamlit web app with inspection tabs
└── tests/                         # Unit tests covering parsing, BM25, RRF, and graph cycles
