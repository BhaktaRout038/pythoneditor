# 🐍 Python 3 Code Editor (Pyodide + CodeMirror)

A lightweight web-based Python 3 code editor built using:

* [Pyodide](https://pyodide.org/) — Python compiled to WebAssembly to run in the browser
* [CodeMirror](https://codemirror.net/) — Syntax highlighting text editor for the browser (removed)

## 🚀 Features

* Python 3 support using Pyodide (no backend required!)
* Syntax highlighting and auto-indentation using CodeMirror
* Error catching with stderr printed in the UI
* Responsive UI (two-column layout, stacks vertically on small screens)
* Output shown in the UI panel (not browser console)

## 📦 CDN Dependencies

* Pyodide 0.24.1 (via jsDelivr)
* CodeMirror 5.65.15 (CSS + Python mode)

## 🔧 How It Works

* `print()` output is redirected using a custom `sys.stdout`/`sys.stderr` class in Python
* `runPythonAsync` is used to execute async Python code
* Errors are captured and shown in the `#output` UI panel

## 🖥️ Usage

1. Open `index.html` in any modern browser (Chrome/Firefox/Edge)
2. Write Python code in the left editor pane
3. Click **Run Python** to see the result in the right pane

## 📁 File Structure

```
.
├── index.html         # Main HTML file with embedded styles and scripts
└── README.md          # This documentation
```

## 🌐 Example Code

```python
print("Hello, World!")

x = "Python"
y = "is"
z = "awesome"
print(x, y, z)
```

## 📌 Limitations

* No `input()` support yet (can be added via JS prompts)
* Limited Python package support (Pyodide base only unless packages are loaded)

## 📄 License

MIT License
