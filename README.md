# eslint-config-finndropstudios

This package provides Finndrop Studios' JS .eslintrc as an extensible shared config.

## Install

Install via npm:

Install the correct versions of each package, which are listed by the command:

```sh
npm info "@finndropstudios/eslint-config@latest" peerDependencies
```

Linux/OSX users can run

```sh
(
    export PKG="@finndropstudios/eslint-config";
    npm info "$PKG@latest" peerDependencies --json | command sed 's/[\{\},]//g ; s/: /@/g' | xargs npm install --save-dev "$PKG@latest"
)
```

Which produces and runs a command like:

```sh
npm install --save dev @finndropstudios/eslint-config eslint@^#.#.# eslint-plugin-import@^#.#.#
```

Windows users can either install all the peer dependencies manually, or use the [install-peerdeps](https://github.com/nathanhleung/install-peerdeps) cli tool.

```sh
npm install -g install-peerdeps
install-peerdeps --dev @finndropstudios/eslint-config
```

## Usage

### eslint-config-finndropstudios

Our configuration contains all of our ESLint rules, including ECMAScript 6+. It requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@uandi/eslint-config"` to your .eslintrc

### eslint-config-finndropstudios/legacy

Lints ES5 and below. Requires `eslint` and `eslint-plugin-import`.

Add `"extends": "@finndropstudios/eslint-config/legacy"` to your .eslintrc
