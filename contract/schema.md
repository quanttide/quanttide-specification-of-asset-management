# 数字资产契约

## 契约

数字资产契约定义项目的资产组成，是项目的资产清单。

契约文件使用YAML格式，默认目录为项目根目录的 `.quanttide/asset/contract.yaml`。

契约字段定义：

- `spec_version`: 契约标准版本。跟随标准文件的发布版本。
- `version`: 资产版本。由用户根据需求自定义。
- `assets`: 资产清单。
- `skills`: 技能清单。

YAML模板：

```yaml
# 契约标准版本：定义解析该文件应遵循哪套标准逻辑
spec_version: 0.0.1  

# 资产版本：定义本项目资产清单当前的演进状态
version: 1.2.0

# 资产清单 
assets:
  <name>:
    title: 资产标题
    description: 资产描述

# 技能清单
skills:
  <name>:
    title: 技能名称
    description: 技能描述 
```

## 资产

数字资产是项目中具有明确权属、可被唯一标识且能通过“数字资产契约”进行索引与调度的逻辑实体。

资产字段定义：

- `name`: 必选。资产标识，作为映射键。
- `title`: 推荐。资产标题。
- `description`: 可选。资产描述。
- `type`: 可选。资产类型。
- `category`: 可选。资产类别。
- `path`: 可选。资产相对路径。


YAML模板：

```yaml
assets:
  <name>:
    title: 资产标题
    description: 资产描述
    type: 资产类型
    category: 资产分类
    path: 资产路径

```

## 技能

数字资产技能是项目中一种可被引用的“能力资产”，它将具体的执行逻辑（如 AI Agent、代码或 API）封装为标准化的语义接口，用于定义项目“能做什么”而非“如何去做”。

技能字段定义：

- `name`: 必选。技能标识，作为映射键。
- `title`: 推荐。技能标题。
- `description`: 推荐。技能描述。
- `type`: 推荐。技能类型。

YAML模板:

```yaml
skills:
  <name>:
    title: 技能描述
    description: 技能描述
    type: 技能类型
```

### 技能类型

技能类型用于标识资产的核心驱动力、环境依赖以及确定性特征。

类型定义：

- `rule`: 规则型。由确定性算法、本地代码或逻辑引擎驱动的技能。
- `bridge`: 桥接型。指代逻辑系统与物理边界或外部实体进行数据交换的连接性技能，包括文件读写、数据库读写、API读写等。
- `agent`: 智能体型。由生成式AI为中心的智能体驱动的非确定性技能。
