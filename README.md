# Polars: Zero to Hero

[![cookiecutter slidev](https://img.shields.io/badge/cookiecutter-slidev-D4AA00?logo=cookiecutter&logoColor=fff)](https://github.com/baggiponte/cookiecutter-slidev)

Source code for the talk *Polars: Zero to Hero* at Agile Lab. Introduction to the [Polars](https://www.pola.rs/) as well as [functime](https://www.functime.ai)

## 🛩️ How to run

### Prerequisites

Make sure you have installed the following:

* [`git`](https://git-scm.com/).
* [`bun`](https://bun.sh/) (but you can use any other JavaScript runtime).
* [`just`](https://just.systems/), a command runner.
  * The [`justfile`](./justfile) contains a bunch of utilities to ease development. Though optional, it's highly recommended.
* [`gh`](https://cli.github.com/), the GitHub CLI.
  * This is optional too, but recommended.

### 1. Clone the repo

```bash
# with github CLI
gh repo clone baggiponte/agilelab-2024-polars

# with git
git clone git@github.com:baggiponte/agilelab-2024-polars
```

> [!NOTE]
>
> 🎬 How to configure SSH
>
> Cloning over SSH is safer. Follow [this guide](https://www.youtube.com/watch?v=5o9ltH6YmtM).
> Alternatively, you can follow the steps in [this](https://github.com/git-merge-workshops/simplify-signing-with-ssh/blob/main/exercises/01-setup-workstation.md) workshop of GitHub's.

### 2. Install the dependencies

```bash
# with the command runner
just install
```

### 3. Open the slideshow locally

```bash
# with the command runner
just preview
```

Visit http://localhost:3030

## 🤗 contributing

### Prerequisites

* Install all of the the dependencies [above](./README.md#%EF%B8%8F-how-to-run) and [`commitizen`](https://commitizen-tools.github.io/commitizen/). `commitizen` is a release management tool. It's used to release new versions.

### Release workflow

1. Fork the repo:

```bash
gh repo fork baggiponte/agilelab-2024-polars
```

2. Create your own branch.

```bash
git checkout -b your-branch-name
```

3. Commit following the [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

4. Before pushing your changes, run the following command to check if the version bump is possible.

```bash
just test-release
```

This will format the slides, try to build them and test whether a version bump is possible.

## 🙏 Credits

- [`slidev`](https://github.com/slidevjs/slidev) is an amazing framework to build slides from markdown and host them.
- [`just`](https://github.com/casey/just) is just a command runner.
- [`commitizen`](https://commitizen-tools.github.io/commitizen/) is a release management tool.
