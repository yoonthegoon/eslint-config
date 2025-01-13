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

### VS Code

For any VS Code users (or users of forks like Windsurf), ensure you have the ESLint extension installed.
If you have already had ESLint installed in the past, give it a once-over to ensure it's installed for Remote-WSL if
you're on Windows.
Make sure you've run `npm install` in your project directory to ensure the ESLint extension can find the configuration.
In your settings, set

- `Eslint: Enable` to `true`
- `Eslint > Format: Enable` to `false`

Now you should see ESLint warnings and errors in your editor.
If this is still not working, after trying with restarting your editor, try running the `ESLint: Restart ESLint Server`
command.
