# eslint-config-cmdn-react

This package provides Airbnb's .eslintrc as an extensible shared config.

## Purpose

This package provides a custom ESLint configuration tailored for React projects using TypeScript. It includes rules and plugins to ensure code quality, consistency, and adherence to best practices.

## Installation

To use this ESLint configuration in your project, follow these steps:

1. Install this custom ESLint config::
   ```bash
   npm install eslint-config-cmdn-react --save-dev
   ```
2. Create an .eslintrc.js file in the root directory of your project and extend this configuration:
   ```
   module.exports = {
    extends: ['eslint-config-cmdn-react'],
    // Other customizations if needed
   };
   ```

## License

This project is licensed under the MIT License.
