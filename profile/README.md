# ReadyCord

## Contribution Guidelines

### 1. Commit Messages
---

#### 1.1 Messages for the `main` branch
---

- Every commit message should follow this format: `{prefix}({scope}): {message}`
	- `prefix` refers to the kind of change that has been made. It may be one of the following:
		- `feat`: A new feature
		- `fix`: A bug fix
		- `refactor`: Changes that did not add any value to the project from a user
		  perspective, but make the code easier to reason about, more concise, etc. (easier
		  for developers to work with)
		- `test`: One or more tests have been added or changed
		- `docs`: Documentation has been added or changed
		- `ci`: Changes to CI/CD
		- `tooling`: Changes to the developer tooling have been made. This includes `*.nix`
		  files, configuration files such as `.gitignore` etc.

	- `scope` only applies in Monorepos and refers to the specific package that has been
	  affected by this change. If multiple packages have been affected, this should be a
	  comma-separated list of the affected packages.

	- `message` should be a concise, to-the-point summary of the change. This should be an
	  imperative, present tense sentence.

- Every commit should have a body describing what has changed in more detail. This should be done
  with bullet points if possible, otherwise whole sentences if necessary. If the change originated
  from an issue, the issue number should also be included.

#### 1.2 Messages for individual Pull Requests
---

- Commit messages should follow the same formatting as described in
  [1.1](#11-messages-for-the-main-branch). However, it is not required.

- Commit messages will all be squased into a final message before being merged into `main`.

### 2. Branch organization and naming conventions
---

- `main` is the "testing" / "developement" branch. Features that are not ready for production but
  actively in developement and usable should land on this branch before going into production.
- Any feature / bug fix / refactor is to be done on a separate branch with the following naming
  convention: `{#issue}-{prefix}/{pr-title}`
	- `#issue` refers to the Issue number on GitHub
	- `prefix` is the same kind of prefix that is also used for commit messages
	- `pr-title` is the title of the pull request that will eventually merge this branch into
	  `main` where spaces are substituted with `-`

### 3. Pull Requests
---

