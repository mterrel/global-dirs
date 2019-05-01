# global-dirs [![Build Status](https://travis-ci.org/sindresorhus/global-dirs.svg?branch=master)](https://travis-ci.org/sindresorhus/global-dirs)

> Get the directory of globally installed packages and binaries

Uses the same resolution logic as `npm` and `yarn`.


## Install

```
$ npm install global-dirs
```


## Usage

```js
const globalDirectories = require('global-dirs');

console.log(globalDirectories.npm.prefix);
//=> '/usr/local'

console.log(globalDirectories.npm.packages);
//=> '/usr/local/lib/node_modules'

console.log(globalDirectories.npm.binaries);
//=> '/usr/local/bin'

console.log(globalDirectories.yarn.packages);
//=> '/Users/sindresorhus/.config/yarn/global/node_modules'
```


## API

### globalDirectories

#### npm
#### yarn

##### packages

Directory with globally installed packages.

Equivalent to `npm root --global`.

##### binaries

Directory with globally installed binaries.

Equivalent to `npm bin --global`.

##### prefix

Directory with directories for packages and binaries. You probably want either of the above.

Equivalent to `npm prefix --global`.


## Related

- [import-global](https://github.com/sindresorhus/import-global) - Import a globally installed module
- [resolve-global](https://github.com/sindresorhus/resolve-global) - Resolve the path of a globally installed module
- [is-installed-globally](https://github.com/sindresorhus/is-installed-globally) - Check if your package was installed globally


## License

MIT © [Sindre Sorhus](https://sindresorhus.com)
