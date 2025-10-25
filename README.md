# ML589 Project

This is a Python project for ML589. It uses uv for dependency management and includes libraries like PyTorch, scikit-learn, Jupyter, Numpy, and Pandas. The dependencies are simply a grab-bag of common python libraries used in AI/ML applications - it can be changed or modified depending on our needs, but will give us a reasonable starting point.

*uv is a newer all-in-one python development tool. uv comes bundled with tools like `pip`, automatically manages python versions. helps a ton with interoperability and reproducibility.*


## Prerequisites

- **GitHub Account**: To clone and contribute to the repository.

## Installation

### 1. Install uv
uv is a fast Python package manager. Install it globally:
- On Windows: Open a PowerShell terminal and run:
  ```PS
  powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
  ```
  Detailed instructions: [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/)

  More uv notes: [https://docs.astral.sh/uv/getting-started/](https://docs.astral.sh/uv/getting-started/)

- On macOS/Linux: Run in terminal:
  ```zsh
  curl -LsSf https://astral.sh/uv/install.sh | sh
  ```

- Verify: Run `uv --version` in your terminal.

- Detailed uv install instructions: [https://docs.astral.sh/uv/getting-started/installation/](https://docs.astral.sh/uv/getting-started/installation/)

- More uv info: [https://docs.astral.sh/uv/getting-started/](https://docs.astral.sh/uv/getting-started/)

### 2. Clone the Repository
Clone this project from GitHub to your local machine:
- Open a terminal (PowerShell on Windows).

- If you have git installed (check with `git --version` in terminal), run:

    - ```git clonehttps://github.com/wesonis/proj_589.git ```

- vscode has git extensions that can do this in a gui if you prefer

- other options for version control include forking and setting up a codespace, or downloading as a .zip file (look for green `<> code` button in github repo, near top right)





- Navigate into the project folder:
  ```
  cd your-repo-name
  ```

### 3. Set Up the Environment
- Run `uv sync` in the project folder. This will:
  - Create a virtual environment.
  - Install dependencies automatically:
    - **PyTorch (torch)**: With CUDA 12.8 support on Windows machines; without CUDA on other operating systems (e.g., macOS, Linux).
    **WARNING** If you do not have a discrete Nvidia GPU and Cuda 12.8 installed, this installation will fail. Message Will if you need help with uv/pyproject setup - we can fall back to cpu-only or get rid of the dependency entirely if its not needed. 
    - **scikit-learn**
    - **Jupyter**
    - **pandas**
- The process uses a global cache, so large packages like PyTorch download only once.

## Usage

- Activate the environment: Run `uv run python` or `uv run jupyter notebook` to start Jupyter.
- Run your scripts: Use `uv run python main.py` (assuming your main file is `main.py`).

## Contributing

### Push and Pull Changes
- **Pull latest changes**: Before working, run `git pull origin main` to get updates.
- **Make changes**: Edit files in your project folder.
- **Stage and commit**: 
  ```
  git add .
  git commit -m "Your commit message"
  ```
- **Push changes**: 
  ```
  git push origin main
  ```
- If you encounter merge conflicts, resolve them in your editor and commit again.

For more help, check [GitHub Docs](https://docs.github.com/en/get-started) or [uv Docs](https://docs.astral.sh/uv/).