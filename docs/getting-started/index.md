# Getting Started with Reasoning Models

This workshop covers uses of Reasoning Models. The workshop includes several example use cases demonstrating how to implement reasoning-based solutions for various business scenarios.

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

### 1. Setup & Environment (00-setup-aoai.ipynb)

Learn how to set up your environment for working with reasoning models:

#### Overview
- Installing required Python packages
- Setting up environment variables
- Testing your Azure OpenAI connection
- Understanding token usage and costs

#### Key Concepts
- Azure OpenAI endpoint and key configuration
- Python package requirements
- Environment variable management
- Basic API connectivity testing
- Token usage monitoring
- Content filter results understanding

### 2. Basic Text Reasoning (01-text-reasoning.ipynb)

Introduction to fundamental concepts through text-based examples:

#### Key Concepts
- **Reasoning Levels**
  - Low: Quick, straightforward responses
  - Medium: Balanced analysis and explanation
  - High: Deep, thorough analysis with detailed rationale
- **Model Interaction**
  - Setting up chat completions
  - Using developer messages
  - Handling responses
  - Managing tokens
- **Response Analysis**
  - Understanding reasoning tokens
  - Evaluating response quality
  - Measuring performance
  - Analyzing token usage

#### Best Practices
- Clear and specific prompt engineering
- Proper response handling and validation
- Effective error management

### 3. Advanced Features (02-advanced-reasoning.ipynb)

Explore advanced capabilities including:

#### Key Features
- **Developer Messages**
  - Setting context and goals
  - Defining model behavior
  - Controlling output format
- **Structured Outputs**
  - JSON schema definition
  - Type validation
  - Response formatting
- **Function Calling**
  - Function definition
  - Parameter handling
  - Response parsing
- **Vision Support**
  - Image analysis
  - Multi-modal reasoning
  - Visual context integration

#### Use Cases
- Data extraction and processing
- Visual analysis and understanding
- System integration and automation

### 4. Model Comparison (03-model-comparison.ipynb)

Compare GPT and Reasoning models across various tasks:

#### Evaluation Criteria
- **Clarity**: Organization, structure, and flow
- **Accuracy**: Factual accuracy and precision
- **Completeness**: Coverage and depth of analysis
- **Analytical Depth**: Reasoning quality and insights
- **Multi-Dataset Synthesis**: Data integration and patterns

#### Usage Guidelines
<ul>
  <li>Choose <strong>GPT Models</strong> for:
    <ul>
      <li>General text generation</li>
      <li>Creative tasks</li>
      <li>Simple Q&amp;A</li>
    </ul>
  </li>
  <li>Choose <strong>Reasoning Models</strong> for:
    <ul>
      <li>Complex analysis</li>
      <li>Multi-step reasoning</li>
      <li>Structured outputs</li>
    </ul>
  </li>
</ul>

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

## Use case model evaluation

When working with these use cases:

1. Start with the README.md in each directory
2. Review the prompt.md file to understand the input format
3. Study the in-depth analysis for detailed Analysis
4. Use Model Comparison (03-model-comparison.ipynb) to compare reasoning model and GPT model outputs using multi dimension evaluation criteria

## Contributing

Want to add a new use case? Follow these steps:

1. Create a new directory under `usecases/`
2. Include:
   - README.md with overview
   - prompt.md with example prompts
   - in-depth analysis document
3. Submit a pull request

## Getting Help

If you encounter issues:
- Check the [Azure OpenAI documentation](https://learn.microsoft.com/azure/ai-services/openai/)
- Review the [Reasoning Models guide](https://learn.microsoft.com/azure/ai-services/openai/how-to/reasoning)
- Submit issues on our GitHub repository
