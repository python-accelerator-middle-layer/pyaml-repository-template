# pyaml-repository-template

Copier template for pyAML repositories.

## Requirements

Install [Copier](https://copier.readthedocs.io/), for example:

```bash
pip install copier
```

## Create a repository from the template

Create a new project directory with:

```bash
copier copy https://github.com/python-accelerator-middle-layer/pyaml-repository-template.git my-project
```

If you are already in the new project directory, use `.` as the destination:

```bash
copier copy https://github.com/python-accelerator-middle-layer/pyaml-repository-template.git .
```

The answers are saved in `.copier-answers.yml` in the generated project.

## Update an existing repository

From a project generated with this template, run:

```bash
copier update
```

With version tags available, this updates to the latest tagged release. To
update to a specific release, provide its tag:

```bash
copier update --vcs-ref 1.0.0
```

To update to the latest commit on the template's default branch, use:

```bash
copier update --vcs-ref HEAD
```

Copier records the template commit used as the previous baseline in
`.copier-answers.yml`. Review the changes and resolve any conflicts before
committing them.

## Create a release

Push a semantic-version tag to create a GitHub Release with automatically
generated release notes:

```bash
git tag -a 1.0.0 -m "Release 1.0.0"
git push origin 1.0.0
```

Tags containing a prerelease suffix, such as `1.1.0-dev.1`, are published as
GitHub prereleases. Release notes are grouped according to `.github/release.yml`.
