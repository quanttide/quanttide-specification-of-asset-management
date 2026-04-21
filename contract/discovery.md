# 发现配置

发现配置定义自动化探测逻辑，用于从指定范围内根据过滤规则识别并构建资产条目。

## 字段

- `scope`: 推荐。范围，发现的物理边界，支持路径或资源标识符。默认值为当前工作目录`["."]`。
- `filters`: 推荐。过滤规则，发现过程中的规则过滤器。
  - `excludes`: 推荐。排除规则，用于屏蔽噪音数据。
- `maps`: 推荐。映射规则，物理文件特征映射为逻辑资产。

## 排除规则 

定义在发现活动中哪些路径或模式应被忽略，从而避免生成无意义的资产条目。

如果一个路径同时命中了 `scope` 和 `exclude`，排除规则具有最高优先级，该路径将不会被识别为资产。

如果一个父目录被 `exclude` 命中了，其下的所有子文件和子目录将自动被忽略，无论子路径是否符合其他包含规则。

匹配支持标准Glob通配符：
- `*`：匹配单个路径层级中的任意字符。
- `**`：匹配跨越多个层级的任意目录或文件。
- `?`：匹配单个字符。

## 映射规则

定义如何将物理文件特征映射为逻辑资产的属性。

如果一个文件同时符合多个匹配（例如一个作为文档示例的 yaml 文件），遵循 “首位命中（First-match）”规则，即YAML中排在前面的规则优先级更高。

分类映射的字段定义如下：

- `name`: 必选。映射规则名称。
- `match`: 必选。Glob 模式，用于识别文件。
- `assign`: 推荐。命中后赋予资产的字段值。

赋值动作可选字段包括：

- `type`: 资产类型映射。
- `category`: 资产类别映射。

## YAML示例

```yaml
discovery:
  scope: ["."]
  filters:
    excludes:
      # 1. 版本控制
      - "**/.git/**"
      
      # 2. 系统冗余
      - "**/.DS_Store"
      - "**/Thumbs.db"
      
      # 3. 常见的环境与依赖
      - "**/node_modules/**"
      - "**/__pycache__/**"
      - "**/venv/**"
      
      # 4. 临时与构建文件
      - "**/dist/**"
      - "**/build/**"
      - "**/*.log"
      - "**/tmp/**"
  maps:
    docs:
      match: "**/*.{md,txt,pdf}"
      assign:
        type: docs
        
    code:
      match: "**/src/**/*.{py,go,java,js}"
      assign:
        type: code
  
    config:
      match: "**/*.{yaml,yml,json,toml}"
      assign:
        type: config
  
    data:
      match: "**/*.{csv,parquet,avro}"
      assign:
        type: data
```
