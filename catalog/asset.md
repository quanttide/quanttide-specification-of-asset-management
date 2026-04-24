# 资产

资产是项目中具有明确权属、可被唯一标识且能索引与调度的物理实体。

## 资产字段

- `id`: 必选，唯一标识符。
- `name`: 必选，名称。
- `title`: 推荐，资产标题。
- `description`: 可选，资产描述。
- `category`: 推荐，资产类别。
- `content`: 可选，资产内容。
- `created_at`: 可选，创建时间。
- `updated_at`: 可选，更新时间。

## YAML 示例

```yaml
asset:
  id: "550e8400-e29b-41d4-a716-446655440000"
  name: "asset-001"
  title: 资产标题
  description: 资产描述
  category: 资产分类
  content: 资产内容
  created_at: "2026-01-01T00:00:00Z"
  updated_at: "2026-01-01T00:00:00Z"
```
