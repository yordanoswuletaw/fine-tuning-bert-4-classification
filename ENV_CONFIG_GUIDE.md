# Installation Guide for Virtual Environments

This guide provides step-by-step instructions to create, activate, delete virtual environments using **venv** and **Conda**, as well as handling dependencies with `requirements.txt`.

---

## 1️⃣ Using `venv` (Python Virtual Environment)

### Create a Virtual Environment
```bash
python -m venv my_env
```

### Activate the Virtual Environment
- **Windows (cmd/PowerShell):**
  ```bash
  my_env\Scripts\activate
  ```
- **Mac/Linux:**
  ```bash
  source my_env/bin/activate
  ```

### Deactivate the Virtual Environment
```bash
deactivate
```

### Delete the Virtual Environment
```bash
rm -rf my_env  # Mac/Linux
rd /s /q my_env  # Windows (cmd)
```

---

## 2️⃣ Using `Conda` (Conda Virtual Environment)

### Create a Conda Environment
```bash
conda create --name my_env python=3.9
```

### Activate the Conda Environment
```bash
conda activate my_env
```

### Deactivate the Conda Environment
```bash
conda deactivate
```

### Delete the Conda Environment
```bash
conda remove --name my_env --all
```

---

## 3️⃣ Install Packages from `requirements.txt`

### Using `venv` and `pip`
```bash
pip install -r requirements.txt
```

### Using `Conda` (with `pip` inside a Conda environment)
```bash
conda activate my_env
pip install -r requirements.txt
```

---

## 4️⃣ Save Installed Packages to `requirements.txt`

### Using `venv` and `pip`
```bash
pip freeze > requirements.txt
```

### Using Conda (`environment.yml` recommended, but `requirements.txt` still works)
```bash
conda activate my_env
pip freeze > requirements.txt
```

For a Conda-native approach:
```bash
conda env export > environment.yml
```

---

## ✅ Best Practices

- Use `venv` for lightweight Python projects.
- Use `Conda` for ML/Data Science projects with dependencies beyond Python packages.
- Use `requirements.txt` for `pip` projects.
- Use `environment.yml` for Conda projects.

---

🚀 **Happy Coding!**

