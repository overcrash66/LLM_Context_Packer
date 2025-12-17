# LLM Context Packer (Repomix)

> "Stop manually opening 15 files and copy-pasting them one by one. Repomix packs your entire codebase into a single AI-ready prompt in <1 second."

**Turn your entire codebase into a single prompt-ready text file.**

## 🚀 Why?
When working with LLMs (ChatGPT, Claude, Gemini), context is everything. You often need to paste multiple files to get a good refactor or answer. Manually copying file content, adding filenames, and formatting is a pain.

**LLM Context Packer** does it for you:
1.  **Traverses** your project.
2.  **Respects** `.gitignore` (no `node_modules`, `.env`, or secrets).
3.  **Formats** everything into an LLM-friendly structure.
4.  **Copies** the result strictly to your clipboard.
5.  **Counts** the tokens so you know if you fit the context window.

## 📦 Installation

```bash
# Clone the repository
git clone
cd llm-context-packer

# Install locally
pip install .
```

## 🛠 Usage

You can use either `llm-context-packer` or the shorter alias `repomix`.

### Basic Usage
Run in your project root. It automatically copies to clipboard.
```bash
repomix .
```

### Options

```bash
# Don't copy to clipboard, just print to stdout
repomix . --no-copy

# Write to a file instead of clipboard
repomix . --output context.txt

# Verbose mode (see what files are being packed)
repomix . --verbose
```

## 📝 Output Format
The tool generates a clean Markdown format that LLMs understand perfectly:

## 🛡 Security
- **Strictly follows `.gitignore`**: If you ignore it in git, it won't be packed.
- **Hidden files ignored**: Skips `.git` directory automatically.
