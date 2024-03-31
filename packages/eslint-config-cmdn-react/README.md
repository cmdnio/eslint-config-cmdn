# eslint-config-cmdn-react

ESLint config for React and Typescript projects by CMDN

## Purpose

This package provides a custom ESLint configuration tailored for React projects using TypeScript. It includes rules and plugins to ensure code quality, consistency, and adherence to best practices.

## Installation

To use this ESLint configuration in your project, follow these steps:

1. Install this custom ESLint config::
   ```bash
   npm install eslint-config-cmdn-react --save-dev
   ```
2. Create an .eslintrc.js file in the root directory of your project and extend this configuration:
   ```ts
   module.exports = {
     extends: ['eslint-config-cmdn-react'],
     // Other customizations if needed
   }
   ```

### Plugins and Rules

### `eslint:recommended`

- [ESLint Recommended Rules](https://eslint.org/docs/rules/)
  - This set of rules includes best practices and guidelines to ensure code quality and maintainability.

### `plugin:@typescript-eslint/strict-type-checked`

- [Strict TypeScript Type-Checking Rules](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/eslint-plugin#supported-rules)
  - This plugin provides rules for strict type-checking in TypeScript code. It helps catch type-related issues at compile-time.

### `plugin:@typescript-eslint/stylistic-type-checked`

- [Stylistic TypeScript Type-Checking Rules](https://github.com/typescript-eslint/typescript-eslint/tree/master/packages/eslint-plugin#supported-rules)
  - These rules focus on stylistic preferences and conventions for TypeScript code, ensuring consistency in code style.

### `next/core-web-vitals`

- [Next.js Core Web Vitals Rules](https://nextjs.org/docs/basic-features/eslint#core-web-vitals)
  - These rules help in identifying and optimizing Core Web Vitals metrics in Next.js applications, focusing on performance improvements.

### `plugin:react-hooks/recommended`

- [React Hooks Rules](https://reactjs.org/docs/hooks-rules.html)
  - These rules enforce best practices and guidelines when using React Hooks, ensuring correct usage and avoiding common pitfalls.

### `plugin:import/errors`

- [Import Plugin Error Rules](https://github.com/benmosher/eslint-plugin-import#rules)
  - This plugin provides rules for handling import statements, helping maintain consistent import patterns and preventing common import-related issues.

### `plugin:import/warnings`

- [Import Plugin Warning Rules](https://github.com/benmosher/eslint-plugin-import#rules)
  - Similar to the error rules, but these rules generate warnings for less critical import-related issues.

### `plugin:import/typescript`

- [Import Plugin TypeScript Rules](https://github.com/benmosher/eslint-plugin-import#typescript)
  - These rules are specifically for TypeScript projects and ensure correct handling of import statements in TypeScript code.

### `plugin:storybook/recommended`

- [Storybook Plugin Rules](https://github.com/storybookjs/eslint-plugin-storybook#usage)
  - This plugin provides rules tailored for Storybook, ensuring consistent and quality code within Storybook stories and configurations.

### `plugin:@tanstack/eslint-plugin-query/recommended`

- [ESLint Plugin Query Rules](https://github.com/tanstack/eslint-plugin-query#rules)
  - This plugin provides rules to improve code quality and maintainability through query-based analysis, allowing for custom linting queries.

### `plugin:sonarjs/recommended`

- [SonarJS Recommended Rules](https://github.com/SonarSource/eslint-plugin-sonarjs#supported-rules)
  - This plugin provides rules based on guidelines from SonarSource to help identify and address code smells and maintainability issues in JavaScript and TypeScript code.

### Customizations

#### `curly`

- Enforces consistent use of curly braces for control statements.

#### `import/default`

- Disables reports for default imports.

#### `import/no-named-as-default`

- Disables reports for named imports using the module name directly.

#### `import/no-useless-path-segments`

- Enforces minimal path segments in imports.
  - Configuration:
    - `noUselessIndex`: true

#### `import/order`

- Enforces a specific order for import statements.
  - Configuration:
    - `groups`: ['builtin', 'external', 'internal', 'parent', 'sibling', 'index', 'object', 'unknown']
    - `newlines-between`: never
    - `alphabetize`:
      - `order`: asc
      - `caseInsensitive`: true

#### `@typescript-eslint/explicit-member-accessibility`

- Disables enforcement of explicit member accessibility.

#### `@typescript-eslint/explicit-function-return-type`

- Disables enforcement of explicit function return types.

#### `@typescript-eslint/no-parameter-properties`

- Disables enforcement of parameter properties.

#### `@typescript-eslint/interface-name-prefix`

- Disables enforcement of interface name prefixes.

#### `@typescript-eslint/explicit-module-boundary-types`

- Disables enforcement of explicit module boundary types.

#### `@typescript-eslint/no-namespace`

- Disables usage of namespaces in TypeScript.

#### `@typescript-eslint/no-explicit-any`

- Disables usage of explicit 'any' types in TypeScript.

#### `@typescript-eslint/no-unused-vars`

- Reports unused variables as warnings, ignoring variables named 'next'.

#### `@typescript-eslint/no-unsafe-assignment`

- Disables reporting of unsafe assignments in TypeScript.

#### `@typescript-eslint/no-unsafe-argument`

- Disables reporting of unsafe arguments in TypeScript.

#### `@typescript-eslint/no-misused-promises`

- Reports misused promises as errors.
  - Configuration:
    - `checksVoidReturn.attributes`: false

#### `@typescript-eslint/prefer-nullish-coalescing`

- Prefers nullish coalescing over logical OR for certain types.
  - Configuration:
    - `ignorePrimitives.boolean`: true

#### `@typescript-eslint/naming-convention`

- Enforces naming convention for certain variable types.
  - Configuration:
    - `selector`: variable
    - `types`: ['boolean']
    - `format`: ['PascalCase']
    - `prefix`: ['is', 'has', 'can', 'should', 'will', 'did']
    - `filter`:
      - `regex`: '^(open|disabled)$'
      - `match`: false

#### `semi`

- Requires semicolons at the end of statements.

#### `quotes`

- Requires single quotes for string literals, avoiding escape.

#### `@next/next/no-img-element`

- Disables the rule 'no-img-element' from the '@next/next' plugin.

## License

This project is licensed under the MIT License.
