# 资产契约

资产契约定义项目的资产组成。

## 资产类型

| 类型 | 说明 |
|------|------|
| `docs` | 文档资产 |
| `code` | 代码资产 |
| `config` | 配置资产 |
| `experiment` | 实验资产 |

## 资产属性

| 属性 | 必填 | 说明 |
|------|------|------|
| `title` | 是 | 资产标题 |
| `type` | 是 | 资产类型 |
| `category` | 是 | 资产分类 |
| `path` | 是 | 资产路径 |
| `description` | 是 | 资产描述 |

## 契约格式

资产契约使用 YAML 格式：

```yaml
assets:
  <asset_key>:
    title: 资产标题
    type: 资产类型
    category: 资产分类
    path: 资产路径
    description: 资产描述
```