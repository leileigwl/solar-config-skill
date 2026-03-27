# 原子库说明

## 文件结构

- `atoms.jsonl` - 全量知识点（JSONL 格式，每行一个 JSON）

## 字段说明

| 字段 | 类型 | 说明 |
|------|------|------|
| `id` | string | 唯一标识 |
| `knowledge` | string | 提炼后的知识点 |
| `original` | string | 原文（可选） |
| `source` | string | 来源（可选） |
| `date` | string | 日期（可选） |
| `topics` | array | 主题标签 |
| `skills` | array | 关联的 skill |
| `type` | string | 类型 |

## type 类型

| 类型 | 说明 |
|------|------|
| `product` | 产品信息（型号、规格） |
| `price` | 价格信息 |
| `knowledge` | 技术知识 |
| `insight` | 行业洞察 |
| `case` | 实际案例 |
| `warning` | 注意事项 |

## topics 主题标签

- `逆变器` - 逆变器相关
- `电池` - 储能电池相关
- `组件` - 光伏组件相关
- `价格` - 价格信息
- `技术` - 技术参数
- `市场` - 市场动态
- `物流` - 物流运输
- `认证` - 认证要求