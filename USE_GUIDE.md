# 多Agent系统使用指南

## 📦 原始项目: agency-agents

GitHub: https://github.com/msitarzewski/agency-agents (9,914 stars)

这是一个**AI Agent 团队模板**，包含 50+ 个专业 Agent，涵盖 9 个部门。

---

## 🏢 Agent 部门一览

### 1. Engineering (工程部) — 7个
| Agent | 用途 |
|-------|------|
| Frontend Developer | React/Vue/Angular 前端开发 |
| Backend Architect | API设计、数据库架构 |
| Mobile App Builder | iOS/Android/React Native |
| AI Engineer | ML模型、AI集成 |
| DevOps Automator | CI/CD、自动化运维 |
| Rapid Prototyper | 快速原型开发 |
| Senior Developer | 复杂技术实现 |

### 2. Design (设计部) — 7个
| Agent | 用途 |
|-------|------|
| UI Designer | 界面设计、组件库 |
| UX Researcher | 用户研究、测试 |
| UX Architect | 架构设计、CSS系统 |
| Brand Guardian | 品牌 identity |
| Visual Storyteller | 视觉叙事 |
| Whimsy Injector | 趣味交互、微动效 |
| Image Prompt Engineer | AI绘图提示词 |

### 3. Marketing (市场部) — 8个
| Agent | 用途 |
|-------|------|
| Growth Hacker | 增长黑客、病毒式营销 |
| Content Creator | 内容创作、编辑日历 |
| Twitter Engager | Twitter 运营 |
| TikTok Strategist | TikTok 策略 |
| Instagram Curator | Instagram 运营 |
| Reddit Community Builder | Reddit 社区运营 |
| App Store Optimizer | ASO 应用商店优化 |
| Social Media Strategist | 社交媒体策略 |

### 4. Product (产品部) — 3个
| Agent | 用途 |
|-------|------|
| Sprint Prioritizer | 敏捷规划、优先级 |
| Trend Researcher | 市场调研、竞品分析 |
| Feedback Synthesizer | 用户反馈分析 |

### 5. Project Management (项目管理) — 5个
| Agent | 用途 |
|-------|------|
| Studio Producer | 高层统筹、组合管理 |
| Project Shepherd | 跨功能协调 |
| Studio Operations | 日常运营优化 |
| Experiment Tracker | A/B测试管理 |
| Senior PM | 需求拆解、范围管理 |

### 6. Testing (测试部) — 7个
| Agent | 用途 |
|-------|------|
| Evidence Collector | 截图QA、视觉验证 |
| Reality Checker | 质量门禁、上线认证 |
| Test Results Analyzer | 测试结果分析 |
| Performance Benchmarker | 性能测试 |
| API Tester | API验证 |
| Tool Evaluator | 工具评估 |
| Workflow Optimizer | 流程优化 |

### 7. Support (支持部) — 6个
| Agent | 用途 |
|-------|------|
| Support Responder | 客服响应 |
| Analytics Reporter | 数据分析、仪表盘 |
| Finance Tracker | 财务管理 |
| Infrastructure Maintainer | 基础设施维护 |
| Legal Compliance Checker | 合规审查 |
| Executive Summary Generator | 高管汇报 |

### 8. Specialized (专精) — 7个
| Agent | 用途 |
|-------|------|
| Agents Orchestrator | **多Agent编排** (核心) |
| Data Analytics Reporter | 数据分析 |
| Data Consolidation Agent | 数据整合 |
| Report Distribution Agent | 报告分发 |
| Sales Data Extraction | 销售数据提取 |
| LSP/Index Engineer | 代码索引 |
| Agentic Identity Trust | 身份信任 |

### 9. Spatial Computing (空间计算) — 6个
| Agent | 用途 |
|-------|------|
| XR Interface Architect | AR/VR 界面设计 |
| visionOS Spatial Engineer | Apple Vision Pro |
| macOS Spatial/Metal Engineer | Mac 3D开发 |
| XR Immersive Developer | WebXR |
| XR Cockpit Interaction | 驾驶舱交互 |
| Terminal Integration | 终端集成 |

---

## 🚀 我们的系统架构

### 当前配置的 Agent

```
┌─────────────────────────────────────────────────────┐
│                    用户 (飞书群)                      │
│              "AI tiktok 工作室"                      │
└─────────────────────┬───────────────────────────────┘
                      │
                      ▼
┌─────────────────────────────────────────────────────┐
│                    Main Agent                        │
│            (统筹调度 - 任务分析 + 分发)                │
└─────────────────────┬───────────────────────────────┘
                      │
     ┌────────────────┼────────────────┐
     ▼                ▼                ▼
┌─────────┐    ┌─────────┐    ┌─────────┐
│Researcher│    │  Coder  │    │ Reporter│
│  (调研)  │    │  (执行)  │    │  (汇报)  │
└─────────┘    └─────────┘    └─────────┘
```

---

## 📋 如何使用

### 方式1: 任务分发 (Main 自动判断)

```
用户: "帮我调研一下TikTok最新热门内容"
      ↓
Main 分析: "调研任务 → 分发给 Researcher"
      ↓
Researcher 执行搜索 → 返回结果
      ↓
Reporter 整理 → 最终回复
```

### 方式2: 手动指定 Agent

```
用户: "@Coder 帮我部署一个网站"
      ↓
Main 直接转给 Coder 执行
      ↓
Coder 完成 → 直接回复
```

### 方式3: 多Agent协作

```
用户: "帮我做个市场调研报告"
      ↓
Main 分发:
  - Researcher: 收集数据
  - Coder: 整理分析
  - Reporter: 生成报告
      ↓
汇总 → 最终回复
```

---

## 🛠️ 配置位置

| 文件 | 路径 |
|-----|------|
| Main 配置 | `/workspace/projects/workspace/cozelx-structure/agents/main.md` |
| Researcher | `/workspace/projects/workspace/cozelx-structure/agents/researcher.md` |
| Coder | `/workspace/projects/workspace/cozelx-structure/agents/coder.md` |
| Reporter | `/workspace/projects/workspace/cozelx-structure/agents/reporter.md` |
| 路由规则 | `/workspace/projects/workspace/config/agents.json` |

---

## 🔄 扩展更多 Agent

如果要添加新的 Agent（比如 TikTok 运营）：

1. 在 `/workspace/projects/workspace/cozelx-structure/agents/` 创建 `tiktok.md`
2. 参考 agency-agents 的 `marketing-tiktok-strategist.md` 格式
3. 更新 `agents.json` 添加路由规则

---

## 📚 参考学习

查看原始项目：
```bash
# 查看所有Agent
ls /workspace/projects/workspace/agency-agents/*/

# 查看核心编排Agent
cat /workspace/projects/workspace/agency-agents/specialized/agents-orchestrator.md

# 查看工程Agent示例
cat /workspace/projects/workspace/agency-agents/engineering/engineering-frontend-developer.md
```
