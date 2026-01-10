# 🚀 UV Package – Complete Documentation (AI/ML Focus)

This documentation is created to help **AI/ML engineers, data scientists, and Python developers** use **`uv`** effectively in real-world projects. You can directly use this as **README.md** for your GitHub repository.

---

## 📌 What is `uv`?

`uv` is a **super-fast Python package manager and virtual environment tool** written in Rust by **Astral**. It is designed as a modern replacement for:

* `pip`
* `pip-tools`
* `virtualenv`
* `venv`
* partially `conda` (for dependency speed, not environments)

### 🔥 Why `uv` is popular in AI/ML

* ⚡ Extremely fast dependency installation (10–100x faster than pip)
* 📦 Deterministic dependency resolution
* 🧠 Handles large AI/ML libraries smoothly (TensorFlow, PyTorch, JAX, etc.)
* 🐍 Better Python version management
* 🔁 Reproducible environments
* 💻 Perfect for research, production, and MLOps

---

## 🛠 Installation

### Windows / Linux / macOS

```bash
pip install uv
```

Or (recommended):

```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

Check installation:

```bash
uv --version
```

---

## 🧪 Core Concepts

| Concept             | Description                              |
| ------------------- | ---------------------------------------- |
| `pyproject.toml`    | Main project config file                 |
| `uv.lock`           | Locked dependencies (like `poetry.lock`) |
| Virtual Environment | Automatically handled                    |
| Resolver            | Very fast & deterministic                |

---

## 📁 Project Initialization

### Initialize a new Python project

```bash
uv init
```

This creates:

* `pyproject.toml`
* `.python-version`

---

## 🧑‍💻 Virtual Environment Management

### Create virtual environment

```bash
uv venv
```

### Activate environment

**Linux / macOS**

```bash
source .venv/bin/activate
```

**Windows**

```powershell
.venv\Scripts\activate
```

### Remove environment

```bash
rm -rf .venv
```

---

## 📦 Package Installation Commands

### Install packages

```bash
uv pip install numpy pandas scikit-learn
```

### Install AI/ML libraries

```bash
uv pip install torch tensorflow keras xgboost lightgbm
```

### Install from requirements.txt

```bash
uv pip install -r requirements.txt
```

### Install editable (local project)

```bash
uv pip install -e .
```

---

## 🔄 Dependency Management

### Freeze dependencies

```bash
uv pip freeze > requirements.txt
```

### Lock dependencies

```bash
uv lock
```

This creates `uv.lock` for **reproducibility**.

### Sync dependencies (very important)

```bash
uv sync
```

> `uv sync` ensures environment matches exactly with lock file.

---

## 🧠 Python Version Management

### Install Python versions

```bash
uv python install 3.10
uv python install 3.11
```

### List installed Python versions

```bash
uv python list
```

### Set project Python version

```bash
uv python pin 3.10
```

---

## 🧾 Running Python & Scripts

### Run Python

```bash
uv run python
```

### Run script

```bash
uv run train.py
```

### Run module

```bash
uv run -m pytest
```

---

## 📊 AI/ML Project Workflow with `uv`

### Typical AI/ML Setup

```bash
uv init
uv venv
uv pip install numpy pandas matplotlib seaborn
uv pip install scikit-learn jupyter notebook
uv pip install torch tensorflow
uv lock
```

### Jupyter Notebook

```bash
uv pip install jupyterlab
uv run jupyter lab
```

---

## ⚙️ pyproject.toml Example (AI/ML)

```toml
[project]
name = "ai-ml-project"
version = "0.1.0"
dependencies = [
    "numpy",
    "pandas",
    "scikit-learn",
    "matplotlib",
    "torch",
    "tensorflow"
]
```

---

## 🔍 Useful Commands Summary

| Command             | Purpose            |
| ------------------- | ------------------ |
| `uv init`           | Create project     |
| `uv venv`           | Create virtual env |
| `uv pip install`    | Install packages   |
| `uv pip uninstall`  | Remove package     |
| `uv lock`           | Lock dependencies  |
| `uv sync`           | Sync environment   |
| `uv python install` | Install Python     |
| `uv python pin`     | Set Python version |
| `uv run`            | Run scripts        |

---

## 🚀 Why Use `uv` for AI/ML Instead of pip/conda?

| Feature     | uv  | pip | conda |
| ----------- | --- | --- | ----- |
| Speed       | ⚡⚡⚡ | ⚡   | ⚡⚡    |
| Lock file   | ✅   | ❌   | ✅     |
| Python mgmt | ✅   | ❌   | ✅     |
| ML-friendly | ✅   | ⚠️  | ✅     |
| Lightweight | ✅   | ✅   | ❌     |

---

## ❌ Common Mistakes

* ❌ Forgetting `uv sync`
* ❌ Mixing `pip` and `uv pip`
* ❌ Not committing `uv.lock`

---

## 📌 Best Practices for AI/ML

* Always commit `uv.lock`
* Use `uv sync` in production
* Pin Python version
* Separate training & inference deps
* Use `uv run` for scripts

---

## 📚 Official Resources

* UV Docs: [https://docs.astral.sh/uv/](https://docs.astral.sh/uv/)
* Astral GitHub: [https://github.com/astral-sh/uv](https://github.com/astral-sh/uv)

---

## ✨ Conclusion

`uv` is a **game-changer** for AI/ML Python projects. It combines speed, reproducibility, and simplicity — making it perfect for **researchers, students, and professionals**.

⭐ If you like this documentation, consider starring the repository!

---

