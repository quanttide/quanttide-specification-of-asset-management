# 量潮数字资产管理标准

## 资产契约

资产契约使用 YAML 格式定义项目的资产组成。

### 基本字段

```yaml
assets:
  <asset_key>:
    title: 资产标题
    type: 资产类型 (docs|code|config|experiment)
    category: 资产分类
    path: 资产路径
    description: 资产描述
```

### 字段说明

| 字段 | 必填 | 说明 |
|------|------|------|
| `title` | 是 | 资产标题 |
| `type` | 是 | 资产类型：docs/code/config/experiment |
| `category` | 是 | 资产分类 |
| `path` | 是 | 资产路径 |
| `description` | 是 | 资产描述 |