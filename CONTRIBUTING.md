# Contribution Guidelines

Here are a few rules to follow in order to ease code reviews, and discussions
before maintainers accept and merge your work.

* [Coding Guidelines](#coding-guidelines)
* [Commit Message Guidelines](#commit-message-guidelines)
* [Merge Request Guidelines](#merge-request-guidelines)

## Terms Definiton

### Type

Must be one of the following:

* feat: A change that introduces a new feature
* fix: A change that fixes a bug
* docs: A changes that fixes, improves, or introduce Documentation
* build: Changes that fixes, improves or introduces build tools
* test: Adding , fixing or improving unit, integ or acceptance tests
* pipeline: Changes that fixes or improves the CI/CD pipeline

### Scope

The scope could be anything specifying place of the commit change.

* part of the domain (gt rcipe)
* part of the documentation (readme or prd)
* part of build tooling (dockerfile or tasksfile)

### Description

The description contains succinct explanation of the change:

* use the imperative, present tense: "change" not "changed" nor "changes"
* don't capitalize first letter
* don't use dot (.) at the end

## Coding Guidelines

Before writing code please read the relevant guidelines from VC engineering handbook (TBA)

## Commit Message Guidelines

Before committing code in this repository it is important to read the guidelines below.

Each commit message consists of  a **type**, a **scope** and a **description** applying the following pattern:

```Bash
<type>(<scope>):<description>
```

Examples:

```bash
git commit -m 'docs(readme): add architeture diagram to the readme'
```

or

```bash
git commit -m 'feat(login): add route to get recip history'
```

## Merge Request Guidelines

Before submitting a merge request to this project it is important to read the guidelines below.

This project implements a template for MR Description and Title in order to achieve the following objectives

* **descriptive title:** from the title of a Merge Request one should be able to infer its goal and scope.
* **contextual description:** from the detailed description a reviewer should be able to understand both technical and functional context.

### Branch

Each branch name consists of  a **type**, a **scope** and a **description** applying the following pattern:

Example:

```bash
<type>/<scope>-<description>
feature/login-google-loging-integration
```

### Merge Request

Each MR title consists of a **type**, a **scope** and a **description** applying the following pattern:

```bash
[<type>/<scope>] <description>
```

Example:

```bash
[Feature/Login] Implement a triage engine to assign products to backlog
```

### Rebase & Squash

 Before merging an MR:

* To avoid merge conflict: task sure you have **rebased from master**
* To clean up history: task sure you **squash all your commits** into one clean final commit
