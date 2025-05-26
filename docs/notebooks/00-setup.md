# Setup & Environment

This notebook guides you through setting up your Azure OpenAI environment for working with reasoning models.

!!! info "Getting Started"
    To run these notebooks:
    1. Clone the [repository](https://github.com/dhangerkapil/reasoning-llms-workshop)
    2. Follow setup instructions in the repository README
    3. Set up your Azure OpenAI endpoint and API key

## Overview

The notebook covers:
1. Installing required Python packages
2. Setting up environment variables
3. Testing your Azure OpenAI connection
4. Understanding token usage and costs

## Key Concepts

### Environment Setup
- Azure OpenAI endpoint and key configuration
- Python package requirements
- Environment variable management

### Model Testing
- Basic API connectivity testing
- Token usage monitoring
- Content filter results understanding

### API Response Analysis
- Response time evaluation
- Token consumption patterns
- Error handling practices

## Prerequisites

Before starting this notebook, ensure you have:
1. An Azure subscription with OpenAI access
2. Python 3.8+ installed
3. Basic understanding of Python and Jupyter notebooks

## Getting Started

1. Create a `.env` file in your workspace with:
```env
AZURE_OPENAI_ENDPOINT=your_endpoint
AZURE_OPENAI_API_KEY=your_key
```

2. Install required packages:
```bash
pip install openai azure-identity python-dotenv
```

3. Run through the notebook cells sequentially

## Next Steps

After completing this notebook, proceed to:
1. [Basic Text Reasoning](01-text-reasoning.ipynb) to learn fundamental concepts
2. [Advanced Features](02-advanced-reasoning.ipynb) to explore more capabilities
3. [Model Comparison](04-model-comparison.ipynb) to understand model differences
