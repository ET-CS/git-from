git-from
========

`git-from` is an extension of git clone,
allowing you to create a new repo based on a template repo.

## Installation

Copy `git-from` into your path. make sure it's executable (`chmod +x git-from`).

## Usage

	git from <repo> <dir>

You can provide your `.git-from` file in the template repo and it will 
be runned once and deleted. `<dir>` will be passed as param.

### Example

Example `.git-from`:

```
#!/bin/bash
NEW_REPO_NAME=$1
echo "preparing repo $NEW_REPO_NAME"
# replace patterns in git-controlled files
git sed -f g template-repo $NEW_REPO_NAME
```
