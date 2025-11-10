# Helper scripts for Alliance machines

## Installation

1. Clone the repository: `git clone https://github.com/vandalt/alliance-helpers.git`
2. Add the `bin` subdirectory to your path. For example, if you cloned the repository in `~/repos`:

```bash
if ! [[ "$PATH" =~ "$HOME/repos/alliance-helpers/bin" ]]
then
  PATH="$HOME/repos/alliance-helpers/bin:$PATH"
fi
```

3. Restart your shell or source the rc file (`source ~/.bashrc` or `source ~/.zshrc`)

## Scripts

- `cvenv`: Load modules, create virtual environment and upgrade pip
- `svenv`: Load modules and source virtual environment. Must be called with `source svenv` to propagate to current shell. Create an alias `alias svenv='source svenv'` in your `~/.bashrc` or `~/.zshrc` if you want `svenv` alone to source the environment.
- `get_deps`: Create `requirements.txt` from `pyproject.toml`
- `pyinstall`: Creates a `.alliance` directory with requirements files for all dependencies (`requirements.txt`), available wheels (`available_wheels.txt`) and missing wheels (`missing_wheels.txt`). Will also download the missing wheels to `.alliance/local-wheels` and install everything with Pip.
- `find_missing_deps`: Script I wrote before realising `avail_wheels` existed. Keeping just in case.
