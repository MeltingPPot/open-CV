# Repository Guidelines

## Project Structure & Module Organization

This is a Chinese-language computer-vision learning workspace. Keep content in the numbered stages:

- `00_学习路线/`: study plans and progress checklists.
- `01_论文阅读/`: paper lists, reading notes, and reference material.
- `02_代码复现/`: reproduction code, baselines, scripts, and templates.
- `03_数据集/`: dataset acquisition, preprocessing, annotation, and version notes.
- `04_笔记/`: concepts, architectures, and training techniques.
- `05_实验记录/`: parameters, metrics, observations, and experiment logs.
- `06_工具与环境/`: environment definitions and dependency lists.
- `07_项目实战/`: small projects and end-to-end demonstrations.
- `assets/` and `outputs/`: reusable visuals and generated artifacts. Raw datasets, runs, checkpoints, and generated outputs are ignored by Git.

## Build, Test, and Development Commands

There is no repository-wide build system. Create the Conda environment with `conda env create -f 06_工具与环境/environment.yml`, then run `conda activate cv-learning`. Alternatively use `pip install -r 06_工具与环境/requirements.txt`. Launch notebooks with `jupyter lab`. Run experiments from their own directory and document the command and configuration in `05_实验记录/`.

## Coding Style & Naming Conventions

Use Python 3.10-compatible code, four spaces for indentation, `snake_case` for files, functions, and variables, and `PascalCase` for classes. Keep scripts small and reproducible: expose paths and hyperparameters as arguments or configuration, avoid hard-coded machine-specific paths, and add concise docstrings for reusable functions. Use UTF-8 and preserve the existing Chinese directory names. No formatter or linter is currently configured; keep imports organized and run a syntax check with `python -m compileall <path>` before committing code.

## Testing Guidelines

No formal test framework or coverage threshold is configured. For code changes, perform a meaningful smoke test (such as one-batch training or inference), verify outputs and tensor shapes, and record dataset, device, seed, and metrics. New tests should use nearby `tests/` directories and `test_*.py` names.

## Commit & Pull Request Guidelines

The existing history uses short, descriptive subject lines (for example, `Initial commit: computer vision learning project`). Keep commits focused and use imperative subjects such as `Add ...` or `Update ...`; avoid committing datasets, credentials, checkpoints, or generated runs. Pull requests should explain the learning or engineering goal, list affected directories, include reproduction commands and validation results, link related issues when applicable, and attach before/after figures for visual or model-output changes.

## Security & Configuration Tips

Keep API keys and local settings in `.env` or untracked configuration files. Do not place credentials, private dataset URLs, or machine-specific absolute paths in notebooks, logs, or committed scripts. Check `.gitignore` before adding large data or model artifacts.
