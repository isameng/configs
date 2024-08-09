# configs 🛠📦

![npm](https://img.shields.io/badge/npm-v1.0.0-blue)

Front-end project configuration tool

</div>

---

## Table of Contents

-   [Installation](#installation)
-   [Usage](#usage)
    -   [config prettier](#config-prettier)
    -   [config eslint](#config-eslint)
    -   [config commitlint](#config-commitlint)
    -   [config tsconfig](#tsconfigjson)

## 安装

```javascript
$ npm install @isameng/configs --save-dev
or
$ npm install @isameng/configs -D
```

## 使用

### config prettier

使用 prettier ，需要创建一个 .prettierrc.cjs 文件，并将以下内容添加到该文件中

```javascript
module.exports = require('@isameng/configs/prettier');
```

### config eslint

使用 eslint + typescript + react ，需要创建一个 .eslintrc.cjs 文件，并将以下内容添加到该文件中

```javascript
module.exports = require('@isameng/configs/eslint-react-ts');
```

使用 eslint + typescript + vue ，需要创建一个 .eslintrc.cjs 文件，并将以下内容添加到该文件中

```javascript
module.exports = require('@isameng/configs/eslint-vue-ts');
```

### config commitlint

使用 commitlint ，需要创建一个 .commitlintrc.cjs 文件，并将以下内容添加到该文件中

```javascript
module.exports = require('@isameng/configs/commitlint');
```

### tsconfig.json

tsconfig.json 基础配置

```json
{
    "extends": "@isameng/configs/base-tsconfig",
    "compilerOptions": {
      /**
        如果需要使用别名，请添加以下配置
        "baseUrl": ".",
        "paths": {
          "@/*": ["src/*"]
        }
       */
    },
    "include": ["src/**/*.ts", "src/**/*.d.ts", "src/**/*.tsx"],
    // vue "include": ["src/**/*.ts", "src/**/*.d.ts", "src/**/*.tsx", "src/**/*.vue"]
    "exclude": ["node_modules", "dist"]
}
```

### TODO

-   [x] eslint config
-   [x] tsconfig
-   [x] prettier
-   [x] commitlint config
