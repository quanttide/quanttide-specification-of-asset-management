# 结构

定义数字资产契约的结构，包括契约文件格式、字段规范和版本管理。

## 契约文件

数字资产契约定义项目的资产组成，是项目的资产清单。

契约文件使用YAML格式，默认目录为项目根目录的 `.quanttide/asset/contract.yaml`。

## 契约字段

- `spec_version`: 契约标准版本。跟随标准文件的发布版本。
- `version`: 资产版本。由用户根据需求自定义。
- `assets`: 资产清单。
- `skills`: 技能清单。
- `discovery`: 发现配置（可选）。
- `registry`: 注册配置（可选）。
- `validation`: 验证配置（可选）。

## YAML模板

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

# 发现配置（可选）
discovery:
  # ... 发现配置

# 注册配置（可选）
registry:
  # ... 注册配置

# 验证配置（可选）
validation:
  # ... 验证配置
```
