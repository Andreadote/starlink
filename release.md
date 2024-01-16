Releases with semantic-versioning
1. Install the semantic-release on your local environment:

 $ npm install --save-dev semantic-release
 $ npm install semantic-release @semantic-release/git @semantic-release/github -D


2. Create a config file (release.config.js) .....in the project with the contents below:

release.config.js
====================

module.exports = {
branches: "main",
repositoryUrl: "https://github.com/Andreadote/actionstest.git",
plugins: [
  '@semantic-release/commit-analyzer',
  '@semantic-release/release-notes-generator',
  '@semantic-release/git',
  '@semantic-release/github']
 }