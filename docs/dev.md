# Development

# Setting up your environment

```bash
python3 -m pip install --user pipx
pipx install pdm
pdm install
pdm install -g ci-quality
pdm run pre-commit install
```

or simply run make install which will execute the above commands.
```bash
make install
```

# Coding
* Your cocotbext code should go in the src/cocotbext.../folder.
* Templates are already present in the folder modify them as per need.
* Always create a feature branch. Read [git branching workflow](https://git-scm.com/book/en/v2/Git-Branching-Branching-Workflows)

# Pre commit checks

In the root of the repo run

```bash
pdm run duty check
```

Fix any warnings that are reported before checking in the code.

Then

```bash
git commit -a
git push
```
*Note:*
1. *NEVER COMMIT BINARY FILES OR FILES GENERATED BY TOOLS*
2. Never run `git add .` or `git add *` always run `git add <filename>`
3. Before writing the commit message see what files are getting committed and what files are ignored. If you see any issue abort the commit, fix the issue and then commit.
4. Before adding any file ask yourself the following questions, If you cannot answer them do not add/commit these files.
	1. "I will need this file after 2 months because..."
	2. This file cannot be generated when needed because ..."
```

# Tasks
1. Create a feature branch called docs and update the document.
2. create feature branch called ext and write the extension code there.
