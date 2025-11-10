# Helper scripts for Alliance machines

- `cvenv`: Load modules, create virtual environment and upgrade pip
- `svenv`: Load modules and source virtual environment. Must be called with `source svenv` to propagate to current shell
- `get_deps`: Create `requirements.txt` from `pyproject.toml`
- `pyinstall`: Creates a `.alliance` directory with requirements files for all dependencies (`requirements.txt`), available wheels (`available_wheels.txt`) and missing wheels (`missing_wheels.txt`). Will also download the missing wheels to `.alliance/local-wheels` and install everything with Pip.
- `find_missing_deps`: Script I wrote before realising `avail_wheels` existed. Keeping just in case.
