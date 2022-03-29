# stylelint

## 支持标准CSS
### 安装依赖
```
npm i -D stylelint stylelint-config-standard
```
- [stylelint](https://github.com/stylelint/stylelint/blob/main/docs/user-guide/get-started.md)
- []()
### 配置
项目根目录下创建.stylelintrc.json
```json
{
    "extends": [
        "stylelint-config-standard"
    ]
}
```

> 注：默认情况下stylelint只支持标准的.css的解析

## 支持SCSS
### 安装依赖
```
npm i -D stylelint-config-standard-scss
```
### 配置
```json
{
    "extends": [
        "stylelint-config-standard-scss"
    ]
}
```

> 注：stylelint-config-standard-scss 依赖 [stylelint-config-standard](https://github.com/stylelint-scss/stylelint-config-standard-scss/blob/main/package.json)

## 支持排序
### 安装依赖
```
npm i -D stylelint-config-recess-order
```
### 配置
```json
{
    "extends": [
        "stylelint-config-recess-order",
        "stylelint-config-standard-scss"
    ]
}
```

> 注: 建议stylelint-config-recess-order在最前面，因为排序是通用的规则

## 支持vue
### 安装依赖
```
npm i -D stylelint-config-standard-vue postcss-html
```
### 配置
```json
{
    "extends": [
        "stylelint-config-recess-order",
        "stylelint-config-standard-scss",
        "stylelint-config-standard-vue"
    ]
}
```

> 注: stylelint-config-standard-vue建议加在最后

## vscode-stylelint配置
### 安装插件
vscode商店搜索stylelint并安装

> 注：建议安装最新的，不支持13.x以及以下版本

### 配置
在项目跟目录下.vscode文件夹下新建settings.json加入如下配置
```
{
    "css.validate": false,
    "less.validate": false,
    "scss.validate": false,
    "stylelint.validate": [
        "css", 
        "scss",
        "vue"
    ],
    "cSpell.words": [
        "stylelint",
        "stylelintrc"
    ]
}
```

> 注：该配置为stylelint14.x版本配置 13.x版本不适用