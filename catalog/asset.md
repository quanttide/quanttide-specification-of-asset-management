# 资产

资产是项目中具有明确权属、可被唯一标识且能通过"数字资产契约"进行索引与调度的逻辑实体。

## 资产字段

- `id`: 必选唯一标识符。
- `title`: 推荐资产标题。
- `description`: 可选资产描述。
- `category`: 推荐资产类别。
- `content`: 可选资产内容。
- `created_at`: 可选创建时间。
- `updated_at`: 可选更新时间。

## 资产类型

常见资产类型：

- `docs`: 文档资产
- `code`: 代码资产
- `config`: 配置资产
- `experiment`: 实验资产

## YAML 示例

```yaml
asset:
  id: "asset-001"
  title: 资产标题
  description: 资产描述
  category: 资产分类
  content: 资产内容
  created_at: "2026-01-01T00:00:00Z"
  updated_at: "2026-01-01T00:00:00Z"
```