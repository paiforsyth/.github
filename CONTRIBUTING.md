# Contributing to CarbonPlan

CarbonPlan is a non-profit. CarbonPlan is a non-profit organization working on
the science and data of carbon removal. We aim to improve the transparency and
scientific integrity of carbon removal and climate solutions through open data
and tools.

This page provides information on how best to contribute.

## Askying questions

*If you have questions about one of CarbonPlan's projects, please post your
question on the appropriate repository issue tracker.*

For reference, we provide a table with some of the main repositories to help
direct questions to the right place.

| Project                 | Issue Tracker                                       |
| ----------------------- | --------------------------------------------------- |
| carbonplan.org          | <https://github.com/carbonplan/carbonplan.org/issues> |
| carbonplan.org/reports  | <https://github.com/carbonplan/reports/issues>        |
| carbonplan.org/research | <https://github.com/carbonplan/research/issues>       |
| api.carbonplan.org      | <https://github.com/carbonplan/api/issues>            |

You can also reach out to CarbonPlan via [email](mailto:feedback@carbonplan.org).

## Bug reports

*If you find a bug in one of our projects, please raise a GitHub issue.*

We find it generally useful to ask for three categories of information.

1. [A minimal, reproducible example describing the problem.](https://stackoverflow.com/help/minimal-reproducible-example).
   If reporting a bug from a website, screenshots are often useful.
1. An explanation of why the current behaviour is wrong/not desired, and what
   you expect instead.
1. Information about the versions of software you are using. If reporting a bug
   from a website, this usually includes which browser you are using.

## Enhancement proposals

*If you have an idea about a new feature or improvement to a CarbonPlan
project, please raise a GitHub issue to first discuss.*

Of course, we welcome ideas and suggestions for how to improve our projects
but keep in mind that we may not be able to address all enhancement proposals.
If you are excited to work on an enhancement yourself, be sure to mention that
in your issue.

## Contributing code

We follow a classic GitHub-centric model for collaborating on software projects.
The basic steps are described below.

### 1. Fork the repository

All of CarbonPlan's software projects are hosted on GitHub. You can
[Fork](https://help.github.com/en/github/getting-started-with-github/fork-a-repo)
any of CarbonPlan's public repositories. Simply click the `Fork` button on the
repository to create a copy that you can edit.

Once you've forked a repository, you can create a local clone via:

```shell
git clone https://github.com/{user-name}/{repo-name}.git
```

### 2. Create a development environment

With a few exceptions, most CarbonPlan projects will require some sort of development
environment to install project dependencies in.

#### Python Projects

For Python projects we recommend using a [Conda](https://docs.conda.io/projects/conda/en/latest/index.html)
virtual environment. This often looks like:

```shell
conda create -n carbonplan ...
conda activate carbonplan
pip install -e .
```

#### For JavaScript Projects

For JavaScript projects, we recommend using [npm](https://www.npmjs.com/) to
install project dependencies.

```shell
npm install .
```

### 3. Creating a branch

Before you get started with your work on a project, its usually a good idea to
checkout a clean branch to work on.

```shell
git fetch upstream
git checkout -b shiny-new-feature upstream/master
```

Then, once your work is ready to share, commit and push to your Fork:

```shell
git add ...
git commit
git push origin shiny-new-feature
```

At this point, you can open a [Pull Request](https://help.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests).

### 4. Running the test suite

Most CarbonPlan projects include a test suite of some kind.

#### Testing Python Projects

For Python projects, we typically use [Pytest](https://docs.pytest.org/en/latest/contents.html).

```shell
py.test -v
```

#### Testing JavaScript Projects

For JavaScript projects, you can test your changes by deploying a local version:

```shell
npm run dev
```

### 5. Code standards and style

Without being overly pedantic about code standards or style, we have adopted a
few general approaches to ensure consistency across our code base. We have
setup automatic formatters in many of our projects using [pre-commit](https://pre-commit.com/).

To run `pre-commit` in a specific project, simply type:

```shell
pre-commit run [--all-files]
```

#### Styling for Python Projects

For Python projects, we use the [Black](https://black.readthedocs.io/en/stable/)
formatter for code styling, along with [flake8](https://flake8.pycqa.org/en/latest/)
and [isort](https://isort.readthedocs.io/en/latest/).

#### Styling for JavaScript Projects

For JavaScript projects, we use [Prettier](https://prettier.io/) and
[StandardJS](https://standardjs.com/).

### 6. Continuous Integration

Continuous integration is the practice of automatically executing tests
whenever changes are made to a project. We use [GitHub Actions](https://github.com/features/actions)
and [Vercel](https://vercel.com/).
