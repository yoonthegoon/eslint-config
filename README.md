# eslint-config

This package provides a shared ESLint configuration for all of our projects.

## Installation

```shell
npm install --save-peer @seriesfi/eslint-config
```

## Usage

Add a `eslint.config.mjs` file to the root of your project with the following contents:

```javascript
import baseConfig from '@seriesfi/eslint-config'

const eslintConfig = [
  ...baseConfig,
  // Add any project-specific overrides here
]

export default eslintConfig
```

Ideally, this package is paired with our [prettier-config](https://github.com/seriesfi/prettier-config) package.
Copy [eslint.yml](/.github/workflows/eslint.yml) to your project.
On pushes, the GitHub Actions workflow will run ESLint on all files and fail if there are any linting errors.
