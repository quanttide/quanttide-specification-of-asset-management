# 资产契约

资产契约定义项目的资产组成。

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

## 字段说明

| 字段 | 必填 | 说明 |
|------|------|------|
| `title` | 是 | 资产标题 |
| `type` | 是 | 资产类型：docs/code/config/experiment |
| `category` | 是 | 资产分类 |
| `path` | 是 | 资产路径 |
| `description` | 是 | 资产描述 |

## 资产类型

| 类型 | 说明 |
|------|------|
| `docs` | 文档资产 |
| `code` | 代码资产 |
| `config` | 配置资产 |
| `experiment` | 实验资产 |

## 示例

```yaml
brd:
  title: 商业需求文档
  type: docs
  category: brd
  path: docs/brd
  description: 创始人知识库迁移痛点、业务场景、成功标准
```