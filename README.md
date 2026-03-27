# solar-config-skill

光伏储能系统配置工具箱。基于行业实战经验提炼，支持户用/工商业光伏储能系统配置。

---

## 工具箱

| Skill | 做什么 |
|---|---|
| `/solar-config` | 主入口，自动路由到合适的工具 |
| `/solar-residential` | 户用配置（≤20kW），家庭/别墅 |
| `/solar-commercial` | 工商业配置（>20kW），工厂/商铺 |
| `/solar-storage` | 储能配置，加电池/纯储能 |

---

## 安装

```bash
# 方法 1：手动安装
git clone https://github.com/leileigwl/solar-config-skill.git /tmp/solar
cp -r /tmp/solar/skills/* ~/.claude/skills/
rm -rf /tmp/solar

# 方法 2：只装单个 skill
cp -r skills/solar-residential ~/.claude/skills/
```

安装后在 Claude Code 中输入 `/solar-config` 或「光伏配置」即可。

---

## 知识库

### 目录结构

```
知识库/
├── 原子库/                     # 结构化知识数据库
│   ├── atoms.jsonl             # 全量知识点
│   └── README.md               # 字段说明
│
└── 设备参数库/                 # 设备规格参数
    └── README.md
```

### 原子库是什么

每个知识原子是一条结构化的知识点：

```json
{
  "id": "solar_001",
  "knowledge": "提炼后的知识点",
  "original": "原文",
  "source": "来源",
  "date": "日期",
  "topics": ["逆变器", "价格"],
  "skills": ["solar-residential"],
  "type": "product/price/knowledge/insight"
}
```

---

## 许可证

本项目采用 MIT 许可证。

---

## 来源

知识来源于光伏行业实战经验，包括逆变器供应商、电池供应商、行业专家的对话记录整理。