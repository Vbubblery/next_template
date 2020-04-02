React 本を読んだ際の開発環境

# .vscode

ワークスペース上で設定しようとおもったけど、github で vscode の設定をあげておいたほうがよさそうなんだね
https://github.com/oukayuka/ReactBeginnersBook-2.0/blob/master/06-lint/03-mysetting/.vscode/settings.json

# Eslint

```
yarn add -D eslint-plugin-react @typescript-eslint/eslint-plugin @typescript-eslint/parser
```

# eslint-config

Eslint の設定もそのまま使用させていただく
https://github.com/oukayuka/ReactBeginnersBook-2.0/blob/master/06-lint/03-mysetting/.eslintrc.js

semi だけ不要にした

# Prettier etc..

Prettier だったり stylelint だったり

```
yarn add -D eslint-config-airbnb eslint-config-prettier eslint-plugin-import  eslint-plugin-jest eslint-plugin-jsx-a11y eslint-plugin-prefer-arrow eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks prettier prettier-stylelint stylelint stylelint-config-prettier stylelint-config-standard stylelint-order prettier-stylelint husky lint-staged
```

package.json にも prettier の設定だったり、commit 時に整形等もいれる

```
  "lint-staged": {
    "*.{js,jsx,ts,tsx}": [
      "eslint --fix",
      "git add"
    ],
    "*.css": [
      "stylelint --fix",
      "git add"
    ]
  },
  "prettier": {
    "bracketSpacing": false,
    "singleQuote": true,
    "trailingComma": "es5"
  }
```
