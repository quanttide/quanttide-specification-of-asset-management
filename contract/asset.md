# 资产

数字资产是项目中具有明确权属、可被唯一标识且能通过"数字资产契约"进行索引与调度的逻辑实体。

## 资产字段

- `name`: 必选。资产标识，作为映射键。
- `title`: 推荐。资产标题。
- `description`: 可选。资产描述。
- `type`: 可选。资产类型。
- `category`: 可选。资产类别。
- `path`: 可选。资产相对路径。

## YAML模板

```yaml
assets:
  <name>:
    title: 资产标题
    description: 资产描述
    type: 资产类型
    category: 资产分类
    path: 资产路径
```

## 资产类型

常见资产类型：

- `docs`: 文档资产
- `code`: 代码资产
- `config`: 配置资产
- `experiment`: 实验资产
