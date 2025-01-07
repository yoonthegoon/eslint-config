# eslint-config

This package provides a shared ESLint configuration for all of our projects.

## Installation

```shell
npm install --save-dev @seriesfi/eslint-config
npx husky init
```

Copy [eslint.yml](/.github/workflows/eslint.yml) to your project and replace [pre-commit](/.husky/pre-commit).

## Usage

On commits, the pre-commit hook will run ESLint on all staged files.
On pushes, the GitHub Actions workflow will run ESLint on all files.
