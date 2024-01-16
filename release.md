Releases with semantic-versioning
1. Install the semantic-release on your local environment:

 $ npm install --save-dev semantic-release
 $ npm install semantic-release @semantic-release/git @semantic-release/github -D
2. Create a config file (release.config.js) in the project with the contents below:

release.config.js
====================

module.exports = {
branches: "main",
repositoryUrl: "https://github.com/Kenmakhanu/actionstest.git",
plugins: [
  '@semantic-release/commit-analyzer',
  '@semantic-release/release-notes-generator',
  '@semantic-release/git',
  '@semantic-release/github']
 }
3. Add your project to the repo:

 git add .
4. Commit your project to the repo using conventional commits. Your commit messages should start with:

   fix:                  ......for a patch version
   feat:                 ......for a minor version
   BREAKING CHANGE:      .......for a major version
5. Add step in the CI workflow:

