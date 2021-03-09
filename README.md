# conventional-commits
https://commitlint.js.org/#/guides-local-setup?id=install-commitlint

# Install and configure if needed
`npm install --save-dev @commitlint/{cli,config-conventional}`
`echo "module.exports = {extends: ['@commitlint/config-conventional']};" > commitlint.config.js`

# Install Husky v5
`npm install husky --save-dev`

# Active hooks
`npx husky install`

# Add hook
`npx husky add .husky/commit-msg "npx --no-install commitlint --edit $1"`

# .husky/commit-msg
If the file .husky/commit-msg already exists, you can edit the file and put this:
`npx --no-install commitlint --edit $1`

# commitizen
https://github.com/commitizen/cz-cli
`sudo npm install -g commitizen`
`commitizen init cz-conventional-changelog --save --save-exact.`

