# Learn Semantic Release

## Table of Contents


## Description

The goal of this project is to be a practical guide for implementing a repository that have proper documentation feature and follow the standard development cycle for better automations, and easier development cycle.

## Topics
What do we cover here? We will cover the implementation of:
1. Conventional Commits
2. Generating Changelogs
3. Automating releases
4. Additional tools to help you learn on the go.

# Repository Setup
## 1. Setup Commitizen
### With Commitizen CLI
1. Install Commitizen using the following script
```sh
npm install -g commitizen
```
2. Setting up your repository to be commitizen friendly
```sh
# npm
commitizen init cz-conventional-changelog --save-dev --save-exact

# yarn
commitizen init cz-conventional-changelog --yarn --dev --exact

# pnpm
commitizen init cz-conventional-changelog --pnpm --save-dev --save-exact
```

**Alternatives:**  
You can follow the standard format, but I prefer to have my own setup:
1. Make your repository commitizen friendly
```sh
# npm
commitizen init @metahub/cz-conventional-commit --save-dev --save-exact

# yarn
commitizen init @metahub/cz-conventional-commit --yarn --dev --exact

# pnpm
commitizen init @metahub/cz-conventional-commit --pnpm --save-dev --save-exact
```
2. Install lacking dependency
```sh
npm i -D conventional-changelog-metahub
```

3. **[OPTIONAL]** Move the settings to `.czrc`.  
Apparently there's no way to separate the config from `package.json` so
you have to do it manually. I personally like to keep things separated.   
You can use the `.czrc` in this project, and remove the `config.commitizen` object in `package.json`.

4. Setup finished  
Now you can start using commitizen and implement CC 1.0 by doing
```sh
npx cz
```

<!-- Add this later -->
<!-- ### Without Commitizen CLI -->
<!-- ## 2. Setup Changelog -->
<!-- ## 3. Setup `semantic-release` -->

# References
1. [Automating Semantic Versioning by Matthew Hodgkins](https://hodgkins.io/automating-semantic-versioning)
2. [Commitizen](https://www.npmjs.com/package/commitizen)