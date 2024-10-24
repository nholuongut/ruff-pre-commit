# ruff-pre-commit

![](https://i.imgur.com/waxVImv.png)
### [View all Roadmaps](https://github.com/nholuongut/all-roadmaps) &nbsp;&middot;&nbsp; [Best Practices](https://github.com/nholuongut/all-roadmaps/blob/main/public/best-practices/) &nbsp;&middot;&nbsp; [Questions](https://www.linkedin.com/in/nholuong/)
<br/>

[![Ruff](https://img.shields.io/endpoint?url=https://raw.githubusercontent.com/nholuong-sh/ruff/main/assets/badge/v2.json)](https://github.com/nholuong-sh/ruff)
[![image](https://img.shields.io/pypi/v/ruff/0.7.0.svg)](https://pypi.python.org/pypi/ruff)
[![image](https://img.shields.io/pypi/l/ruff/0.7.0.svg)](https://pypi.python.org/pypi/ruff)
[![image](https://img.shields.io/pypi/pyversions/ruff/0.7.0.svg)](https://pypi.python.org/pypi/ruff)

A [pre-commit](https://pre-commit.com/) hook for [Ruff](https://github.com/nholuong-sh/ruff).

Distributed as a standalone repository to enable installing Ruff via prebuilt wheels from
[PyPI](https://pypi.org/project/ruff/).

### Using Ruff with pre-commit

To run Ruff's [linter](https://docs.nholuong.sh/ruff/linter) and [formatter](https://docs.nholuong.sh/ruff/formatter)
(available as of Ruff v0.0.289) via pre-commit, add the following to your `.pre-commit-config.yaml`:

```yaml
repos:
- repo: https://github.com/nholuongut/ruff-pre-commit.git
  # Ruff version.
  rev: v0.7.0
  hooks:
    # Run the linter.
    - id: ruff
    # Run the formatter.
    - id: ruff-format
```

To enable lint fixes, add the `--fix` argument to the lint hook:

```yaml
repos:
- repo: https://github.com/nholuongut/ruff-pre-commit.git
  # Ruff version.
  rev: v0.7.0
  hooks:
    # Run the linter.
    - id: ruff
      args: [ --fix ]
    # Run the formatter.
    - id: ruff-format
```

To avoid running on Jupyter Notebooks, remove `jupyter` from the list of allowed filetypes:

```yaml
repos:
- repo: https://github.com/nholuongut/ruff-pre-commit.git
  # Ruff version.
  rev: v0.7.0
  hooks:
    # Run the linter.
    - id: ruff
      types_or: [ python, pyi ]
      args: [ --fix ]
    # Run the formatter.
    - id: ruff-format
      types_or: [ python, pyi ]
```

When running with `--fix`, Ruff's lint hook should be placed _before_ Ruff's formatter hook, and
_before_ Black, isort, and other formatting tools, as Ruff's fix behavior can output code changes
that require reformatting.

When running without `--fix`, Ruff's formatter hook can be placed before or after Ruff's lint hook.

(As long as your Ruff configuration avoids any [linter-formatter incompatibilities](https://docs.nholuong.sh/ruff/formatter/#conflicting-lint-rules),
`ruff format` should never introduce new lint errors, so it's safe to run Ruff's format hook _after_
`ruff check --fix`.)

# 🚀 I'm are always open to your feedback.  Please contact as bellow information:
### [Contact ]
* [Name: nho Luong]
* [Skype](luongutnho_skype)
* [Github](https://github.com/nholuongut/)
* [Linkedin](https://www.linkedin.com/in/nholuong/)
* [Email Address](luongutnho@hotmail.com)

![](https://i.imgur.com/waxVImv.png)
![](Donate.png)
[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/nholuong)

# License
* Nho Luong (c). All Rights Reserved.🌟
