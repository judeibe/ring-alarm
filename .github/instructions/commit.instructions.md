## Commit Message Formats

### Default

```text
<type>(<optional scope>): <description>

<body>

<footer>
```

### Merge Commit


```text
Merge branch '<branch name>'
```

*Follows default git merge message*

### Revert Commit

```text
Revert "<reverted commit subject line>"
```

*Follows default git revert message*

### Initial Commit

```commit
chore: init
```

---

## Types

* **feat**: Commits that add or remove a new feature to the API or UI
* **fix**: Commits that fix an API or UI bug in a preceding `feat` commit
* **refactor**: Commits that rewrite or restructure your code without changing API or UI behavior

  * **perf**: A special `refactor` commit that improves performance
* **style**: Commits that do not affect the meaning (whitespace, formatting, missing semicolons, etc.)
* **test**: Commits that add missing tests or correct existing tests
* **docs**: Commits that affect documentation only
* **build**: Commits that affect build components (build tool, CI pipeline, dependencies, project version, etc.)
* **ops**: Commits that affect operational components (infrastructure, deployment, backup, recovery, etc.)
* **chore**: Miscellaneous commits (e.g., modifying `.gitignore`)

## Scopes

The `scope` provides additional contextual information.

* An **optional** part of the format
* Allowed scopes depend on the specific project
* Do not use issue identifiers as scopes

## Breaking Changes Indicator

Breaking changes should be indicated by an `!` before the `:` in the subject line, e.g.:

```text
feat(api)!: remove status endpoint
```

* An **optional** part of the format

### Description

The `description` contains a concise summary of the change.

* **Mandatory**
* Use the imperative, present tense (e.g., “change” not “changed” nor “changes”)
* Do not capitalize the first letter
* Do not end with a period

### Body

The `body` should include the motivation for the change and contrast it with previous behavior.

* **Optional**
* Use the imperative, present tense
* Mention issue identifiers and their relations here

### Footer

The `footer` should contain any information about **Breaking Changes** and references to **Issues**.

* **Optional**
* Optionally reference an issue by its ID
* **Breaking Changes** should start with `BREAKING CHANGES:` followed by a space or two newlines, then the description

## Versioning

* **If** your next release contains commits with:

  * **Breaking changes**, increment the **major version**
  * **API-relevant changes** (`feat` or `fix`), increment the **minor version**
* **Else**, increment the **patch version**

## Examples

```commit
feat: add email notifications on new direct messages
```

```commit
feat(shopping cart): add the amazing button
```

```commit
feat!: remove ticket list endpoint

refers to JIRA-1337

BREAKING CHANGES: ticket endpoints no longer support listing all entities.
```

```commit
fix(shopping-cart): prevent ordering an empty shopping cart
```

```commit
fix(api): fix wrong calculation of request body checksum
```

```commit
fix: add missing parameter to service call

The error occurred because of <reasons>.
```

```commit
perf: decrease memory footprint for determining unique visitors by using HyperLogLog
```

```commit
build: update dependencies
```

```commit
build(release): bump version to 1.0.0
```

```commit
refactor: implement Fibonacci number calculation using recursion
```

```commit
style: remove empty line
```