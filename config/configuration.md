# Hugo 配置

## 单文件配置

单文件配置没什么太大困难，官方文档给出的配置一般为单文件配置

## 配置目录

单个配置文件维护性太差，故采用 `config/` 来进行配置，将配置项模块化。

使用配置目录记住你在单文件中使用的表（map） `[]`，需要即爱那个对应表明转换为一个单配置文件在该环境下

> 有些时候需要区分站点生成环境，所以采用下方这样的配置来进行划分，将站点生成环境区分开来。
> 
> 提示：下方的 `production/`，`staging/` 为 Hugo 环境，我们可以使用 `hugo --environment staging` 按照 `staging/` 中的配置来生产站点（这个过程中 会合并默认配置 `_default/` 下的配置，但是 `staging/` 下的配置优先级为最高）。

```txt
├── config
│   ├── _default
│   │   ├── config.toml
│   │   ├── languages.toml
│   │   ├── menus.en.toml
│   │   ├── menus.toml
│   │   ├── build.toml
│   │   └── params.toml
│   ├── production
│   │   ├── config.toml
│   │   └── params.toml
│   │   ├── build.toml
│   └── staging
│       ├── config.toml
│       └── params.toml
```

> 默认环境为 **开发环境（development）** 为`hugo server`，**生产环境** 即使用 `hugo` 命令。

## 所有配置项 

请直接参考[默认配置文件](./_default/config.toml "默认配置文件")

