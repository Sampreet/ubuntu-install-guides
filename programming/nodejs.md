# Node.js

![Node.js](https://img.shields.io/node/v/gh-badges.svg)

## About

[Node.js and NPM via NVM](https://github.com/creationix/nvm) - Node.js uses event-driven, non-blocking I/O model. NPM is the package manager for JavaScript.

## Installing NVM

To install or update nvm via terminal, use the install script using cURL:
```
curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
```
or Wget:
```
wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.31.1/install.sh | bash
```

## Installing Node.js

To install a specific version of Node.js, say v6.1.0:
```
nvm install 6.1.0
```

## Changing Version

To change the current version running to another, say v4.2:
```
nvm use 4.2
```

## Getting the Path

To get the path to the executable where a version of Node.js, say v5.0, was installed:
```
nvm which 5.0
```

## Migraing NPM Packages

To install a new version ```v2``` of Node.js ad migrate npm packages from a previous version ```v1```:
```
nvm install v2 --reinstall-packages-from=v1
```
