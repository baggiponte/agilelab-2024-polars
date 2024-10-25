# Polars: Zero To Hero

[![cookiecutter slidev](https://img.shields.io/badge/cookiecutter-slidev-D4AA00?logo=cookiecutter&logoColor=fff)](https://github.com/baggiponte/cookiecutter-slidev)

Source code for the talk *Polars: Zero To Hero* at Agile Lab.

## 🛩️ How to run

### Prerequisites

Make sure you have installed the following:

* [`git`](https://git-scm.com/).
* [`node.js`](https://nodejs.org/en/download/package-manager) or [`bun`](https://bun.sh/).

Recommended:

* [`gh`](https://cli.github.com/), the GitHub CLI.
* [`just`](https://just.systems/), a command runner.

### 1. Clone the repo

```bash
# with github CLI
gh repo clone baggiponte/agilelab-2024-polars

# with git
git clone git@github.com:baggiponte/agilelab-2024-polars
```

> **Note**
>
> 🎬 How to configure SSH
>
> Cloning over SSH is safer. Follow [this guide](https://www.youtube.com/watch?v=5o9ltH6YmtM).
> Alternatively, you can follow the steps in [this](https://github.com/git-merge-workshops/simplify-signing-with-ssh/blob/main/exercises/01-setup-workstation.md) workshop from GitHub.


### 2. Install the dependencies

```bash
# with the command runner
just install

# with npm
npm install

# with bun
bun install
```

### 3. Preview the slideshow locally

```bash
# with the command runner
just preview

# with npx
npx slidev --open -- slides.md

# with bun
bun slidev --open -- slides.md
```

Visit http://localhost:3030 to preview the slideshow.

## 🤗 contributing

Install the dependencies [above](,/README.md#%EF%B8%8F-how-to-run) (`just` is highly recommended) and the following:

* [`commitizen`](https://commitizen-tools.github.io/commitizen/) is a release management tool. It's used to release new versions.

1. Fork the repo
2. Create your own branch.
3. Before opening a PR, run the following:

```bash
just test-release
```

This will format the slides, try to build them and test whether a version bump is possibile.

> **Note**
>
> Credits:
>
> - [`slidev`](https://github.com/slidevjs/slidev) is an amazing framework to build slides from markdown and host them.
> - [`just`](https://github.com/casey/just) is just a command runner.
> - [`commitizen`](https://commitizen-tools.github.io/commitizen/) is a release management tool.
