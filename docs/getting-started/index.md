# Getting Started with Reasoning Models

This workshop covers uses of Reasoning Models with Azure OpenAI. The workshop includes several example use cases demonstrating how to implement reasoning-based solutions for various business scenarios.

## Setup Instructions
To get started with this workshop:

1. Visit the [GitHub repository](https://github.com/dhangerkapil/reasoning-llms-workshop)
2. Follow the setup instructions in the README to:
   - Clone the repository
   - Install required dependencies
   - Set up your Azure OpenAI endpoint and API key
   - Configure your environment

## Workshop Materials
All workshop materials, including Jupyter notebooks, are available in the [GitHub repository](https://github.com/dhangerkapil/reasoning-llms-workshop):

### Notebooks
- `00-setup-aoai.ipynb`: Environment setup and Azure OpenAI configuration
- `01-text-reasoning.ipynb`: Basic text reasoning examples
- `02-advanced-reasoning.ipynb`: Advanced features and techniques
- `04-model-comparison.ipynb`: Comparing Reasoning Models with GPT models
- Understand token usage and model responses

### 2. Basic Text Reasoning (01-text-reasoning.ipynb)
Explore:
- Core concepts of reasoning models
- Text-based prompts and responses
- Different reasoning levels (low, medium, high)
- Comparing model outputs and performance

### 3. Advanced Features (02-advanced-reasoning.ipynb)
Master advanced capabilities:
- Developer Messages for context setting
- Structured Outputs for formatted responses
- Function Calling for external integrations
- Vision Support for image analysis
- Multi-modal reasoning tasks

### 4. Model Comparison (04-model-comparison.ipynb)
Learn to:
- Compare GPT and Reasoning model outputs
- Evaluate response quality and accuracy
- Analyze reasoning patterns and depth
- Choose the right model for your use case

## Prerequisites

Before starting:
1. Ensure you have an Azure account with OpenAI access
2. Install required Python packages:
   ```bash
   pip install openai azure-identity python-dotenv
   ```
3. Set up your `.env` file with:
   ```
   AZURE_OPENAI_ENDPOINT=your_endpoint
   AZURE_OPENAI_API_KEY=your_key
   ```

## Getting Help

If you encounter issues:
- Check the [Azure OpenAI documentation](https://learn.microsoft.com/azure/ai-services/openai/)
- Review the [Reasoning Models guide](https://learn.microsoft.com/azure/ai-services/openai/how-to/reasoning)
- Submit issues on our GitHub repository
