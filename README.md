# Javascript
Files for help getting started with javascript

## Setup Linting and Formatting:

- **Ensure npx is installed using ```npm install -g npx```**
- **If using npm in wsl run ```npm config set unsafe-perm=true```**

Install Linter and formatter
- `npm install --only=dev --save eslint prettier eslint-config-prettier eslint-plugin-prettier`

Initilise ESLint
- `npx eslint --init`

For installing Airbnb (if needed and not done through the ESLint init):
- `npx install-peerdeps --only=dev --save eslint-config-airbnb-base`

### .eslintrc.json

Ensure these are in the ESLint config file

```
"extends": ["airbnb-base", "plugin:prettier/recommended"],
```

```
"rules": {
  "prettier/prettier": ["warn", { "printWidth": 120 }],
  "no-restricted-syntax": ["error", "LabeledStatement", "WithStatement"] // NOT "ForInStatement"
}
```
