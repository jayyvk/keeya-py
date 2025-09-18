# Keeya Development Guide

## Quick Start

1. **Set up environment:**
   ```bash
   python setup.py
   ```

2. **Add your OpenRouter API key:**
   ```bash
   export OPENROUTER_API_KEY="your_actual_key_here"
   ```

3. **Test the installation:**
   ```bash
   python test_keeya.py
   ```

## Development Workflow

### 1. Install Dependencies
```bash
pip install -r requirements.txt
pip install -e .
```

### 2. Set Environment Variables
```bash
export OPENROUTER_API_KEY="your_openrouter_key_here"
```

### 3. Test Basic Functionality
```python
import keeya
import pandas as pd

# Test basic code generation
code = keeya.generate("function to add two numbers")
print(code)

# Test with DataFrame
df = pd.DataFrame({'a': [1, 2, 3], 'b': [4, 5, 6]})
cleaned_df = keeya.clean(df)
```

## API Reference

### `keeya.generate(prompt)`
Generate Python code from natural language.

### `keeya.clean(df)`
AI-powered data cleaning.

### `keeya.analyze(df)`
AI-powered data analysis.

### `keeya.visualize(df, plot_type=None)`
AI-powered visualization.

### `keeya.train(df, target)`
AI-powered ML training.

## File Structure

```
keeya/
├── __init__.py          # Main API exports
├── core.py             # Core functionality
├── utils.py            # Utility functions
└── prompts.py          # System prompts
```

## Testing

Run the test script:
```bash
python test_keeya.py
```

## Troubleshooting

### API Key Issues
- Make sure `OPENROUTER_API_KEY` is set
- Check that the key is valid
- Ensure you have credits in your OpenRouter account

### Import Issues
- Make sure you're in the project directory
- Run `pip install -e .` to install in development mode
- Check Python version (3.8+ required)

### Code Execution Issues
- Check that all dependencies are installed
- Verify that the generated code is valid Python
