# Secret Hunter and Replacement Programs

## Overview
These Python scripts help identify and replace sensitive information (e.g., API keys) in `.py` files within your project. Use them to maintain security by locating and scrubbing sensitive data.

---

## Scripts

### 1. `secret_hunter.py`
A tool to scan all `.py` files in the current directory and subdirectories for sensitive keywords like `"API"` or `"key"`.

#### Features
- Identifies potential sensitive data like API keys.
- Excludes specified directories (e.g., `env`, `site-packages`) and itself from scanning.
- Provides detailed output with file paths and line numbers.

#### How to Use
   1. Place `secret_hunter.py` in your project directory.
   2. Run it:
   ```bash
   python secret_hunter.py

3. Review the output for flagged occurrences.

Example Output

[WARNING] Found 'API' in ./example.py, line 10:
  api_key = "12345"  # Your API key

2. replace_secrets.py

A script to automatically replace sensitive strings (e.g., API keys) with placeholders like "your API key here".

Features
   •  Replaces identified sensitive strings directly in .py files.
   •  Uses customizable regex patterns to locate sensitive data.
   •  Safeguards the original file structure while making replacements.

How to Use
   1. Place replace_secrets.py in your project directory.
   2. Update the script to define the sensitive patterns to replace (if needed).
   3. Run it:

   python replace_secrets.py


   4. The program will modify .py files in place, replacing sensitive data.

Default Replacement

Sensitive strings are replaced with:

"your API key here"

Customizing Patterns

Both scripts rely on regular expressions to match sensitive data. You can adjust the patterns in the scripts to meet your specific needs.

Best Practices
   1. Use with Caution:
   •  Always back up your codebase before running replace_secrets.py.
   •  Test your project after replacements to ensure functionality.
   2. Combine with Git Tools:
   •  Use tools like git-secrets or pre-commit to prevent committing sensitive data.
   3. Secure Sensitive Data:
   •  Store sensitive keys in environment variables or configuration files ignored by .gitignore.

   Contributors
   •  Andrew: Built and maintained the scripts.
   •  Feel free to expand functionality or report issues!

   License

MIT License. Modify and distribute freely with attribution.