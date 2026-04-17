# 资产契约

## 什么是资产契约

资产契约定义项目的资产组成，是项目的资产清单。

资产契约是项目的"资产宪法"，定义了项目包含哪些资产。

资产契约位于项目根目录的 `.quanttide/asset/contract.yaml`。

文件内容使用 YAML 格式，包含 `assets` 键，值为资产映射。

## 资产定义

### 资产属性

每个资产项包含以下属性：

| 属性 | 必填 | 说明 |
|------|------|------|
| `title` | 是 | 资产标题 |
| `type` | 是 | 资产类型 |
| `category` | 是 | 资产分类 |
| `path` | 是 | 资产路径 |
| `description` | 是 | 资产描述 |

### 格式

```yaml
assets:
  <asset_key>:
    title: 资产标题
    type: 资产类型
    category: 资产分类
    path: 资产路径
    description: 资产描述
```