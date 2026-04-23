# 契约

以数字资产契约为中心构建数字资产治理规则，包括资产的发现、注册、验证等生命周期管理过程。

## 建模

## 发现

## 契约文件

数字资产契约定义项目的资产组成，是项目的资产清单。

契约文件使用 YAML 格式，默认目录为项目根目录的 `.quanttide/asset/contract.yaml`。

## 契约字段

- `spec_version`: 必选。契约标准版本。跟随标准文件的发布版本。
- `version`: 推荐。资产版本。由用户根据需求自定义。
- `assets`: 推荐。资产清单。
- `skills`: 推荐。技能清单。
- `workflows`: 推荐。工作流清单。
- `discovery`: 推荐。发现配置。
- `registry`: 推荐。注册配置。
- `validation`: 推荐。验证配置。

## YAML示例

```yaml
# 契约标准版本：定义解析该文件应遵循哪套标准逻辑
spec_version: 0.0.4

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

workflows:
  <name>:
    title: 工作流名称
    description: 工作流描述

# 发现配置
discovery:
  scope: ['.']
  filter: 
    excludes: 
      # 过滤规则
  maps:
    <name>:
      match: "<glob>"
      assign: 
        type: "<type>"
        category: "category"

# 注册配置
registry:
  # ... 注册配置

# 验证配置
validation:
  # ... 验证配置
```