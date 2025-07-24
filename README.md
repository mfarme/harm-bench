# HarmBench

A comprehensive evaluation framework for testing generative language models' ability to detect and appropriately respond to harm to self or others in conversational data. 

## Purpose

This system generates hybrid synthetic mental health conversations with ground truth labels and evaluates models on their ability to:
- Detect type of harm (self-harm, harm to others)
- Make appropriate escalation decisions
- Provide consistent and reliable assessments

## Key Features

- **CLI interface**: Utilize HarmBench to create your own hybrid datasets, use exisiting data, change the models, and examine evaluation results. 
- **Hybrid Data Generation**: Annotated Reddit dataset as conversation starter to generate conversations with realistic personas and scenarios
- **Multi-Model Evaluation**: Support for OpenAI, Anthropic, Google, and Ollama models
- **Ground Truth Labeling**: Automated labeling with harm categorization and severity levels when applicable
- **Performance Assessment**: Comprehensive metrics including precision, recall, F1, sensitivity, specificity, and escalation accuracy
- **Batch Processing**: Scalable evaluation with configurable distributions and formats
- **MCP Integration**: Model Context Protocol tool for escalation and human simulation

## Quick Start

### Installation

```bash
# Clone the repository
git clone <repository-url>
cd harm-bench

# Create virtual environment
python -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt

# Set up environment variables
cp .env.example .env
# Edit .env with your API keys for OpenAI, Anthropic, and Google Gemini, optional Ollama integration
```

### Running Tests

```bash
# Run all tests
python -m pytest tests/

# Run specific test suites
python -m pytest tests/test_end_to_end_integration.py  # Integration tests
python -m pytest tests/test_performance_suite.py       # Performance tests
python -m pytest tests/test_validation_suite.py        # Validation tests
```

## Project Structure

```
harm-bench/
├── evaluation/                    # Core package
│   ├── core/                      # Core interfaces and models
│   ├── data_generation/           # Conversation generation
│   ├── model_evaluation/          # Model adapters and evaluation
│   ├── assessment/                # Metrics and analysis
│   └── mcp_tools/                 # MCP integration tools
├── tests/                         # Test suite
├── config/                        # Configuration files
├── data/                          # Input data and External Data
├── demo_output/                   # Demo outputs
├── secure_data/                   # Encrypted data storage
└── requirements.txt               # Dependencies
```

## Documentation

- CLI Usage Guide

## Target Users

- AI researchers evaluating mental health applications
- Mental Health organizations deploying conversational AI
- Model developers testing safety and reliability
- Regulatory bodies assessing AI safety in healthcare

## Citation

## License

MIT

## Contributing
