# 数字资产契约

资产契约使用 YAML 格式定义项目的资产组成。

## 基本字段

```yaml
assets:
  <asset_key>:
    title: 资产标题
    type: 资产类型 (docs|code|config|experiment)
    category: 资产分类
    path: 资产路径
    description: 资产描述
```

详见 [asset.md](asset.md)