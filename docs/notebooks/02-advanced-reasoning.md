# Advanced Features

This notebook explores advanced capabilities of reasoning models, including structured outputs, function calling, and vision support.

!!! info "Getting Started"
    To run these notebooks:
    1. Clone the [repository](https://github.com/dhangerkapil/reasoning-llms-workshop)
    2. Follow setup instructions in the repository README
    3. Set up your Azure OpenAI endpoint and API key

## Overview

Learn advanced features:
1. Developer Messages
2. Structured Outputs
3. Function Calling
4. Vision Support

## Key Features

### Developer Messages
- Setting context and goals
- Defining model behavior
- Controlling output format

### Structured Outputs
- JSON schema definition
- Type validation
- Response formatting

### Function Calling
- Function definition
- Parameter handling
- Response parsing

### Vision Support
- Image analysis
- Multi-modal reasoning
- Visual context integration

## Implementation Examples

### 1. Structured Data Extraction
```python
class CalendarEvent(BaseModel):
    name: str
    date: str
    participants: list[str]
```

### 2. Vision Analysis
```python
messages=[
    {"role": "user", "content": [
        {"type": "text", "text": "Describe this image"},
        {"type": "image_url", "image_url": {"url": "image.jpg"}}
    ]}
]
```

## Best Practices

1. **Structured Outputs**
   - Define clear schemas
   - Validate responses
   - Handle errors gracefully

2. **Function Calling**
   - Use descriptive names
   - Document parameters
   - Include error handling

3. **Vision Support**
   - Provide clear prompts
   - Consider image context
   - Handle multi-modal data

## Use Cases

1. **Data Extraction**
   - Form processing
   - Document analysis
   - Information structuring

2. **Visual Analysis**
   - Image description
   - Object detection
   - Scene understanding

3. **Function Integration**
   - API automation
   - Data processing
   - System integration

## Next Steps

1. Try the [Model Comparison](04-model-comparison.ipynb) notebook
2. Explore practical use cases
3. Build your own applications
