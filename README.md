# Description

This project aims to exemplify the use of Conventional Commits using tools such as: commitlint, commitizen and commitsar

## Conventional-commits
- https://commitlint.js.org/#/guides-local-setup?id=install-commitlint
- https://github.com/conventional-changelog/commitlint
- https://www.conventionalcommits.org/en/v1.0.0/


## to run local
- clone the project
- run npm install to generate node-models
- to commit use `git cz`
- verify commits (to CI/CD): `docker run --rm --name="commitsar" -w /src -v "$(pwd)":/src aevea/commitsar commitsar .`

# Install in yours projects

## Install and configure if needed
`npm install --save-dev @commitlint/{cli,config-conventional}`
`echo "module.exports = {extends: ['@commitlint/config-conventional']};" > commitlint.config.js`

## Install Husky v5
`npm install husky --save-dev`

## Active hooks
`npx husky install`

## Add hook
`npx husky add .husky/commit-msg "npx --no-install commitlint --edit $1"`

## .husky/commit-msg
If the file .husky/commit-msg already exists, you can edit the file and put this:
`npx --no-install commitlint --edit $1`

## commitizen
https://github.com/commitizen/cz-cli

`sudo npm install -g commitizen`
`commitizen init cz-conventional-changelog --save --save-exact.`

## to commit

`git cz`

# commitsar
`docker run --rm --name="commitsar" -w /src -v "$(pwd)":/src aevea/commitsar commitsar .`

2.1.4

(2) - MAJOR: API Publica
(1) - MINOR: Add funcionalidades, mas compatível com a API
(4) - PATCH: Bugs, ajustes
