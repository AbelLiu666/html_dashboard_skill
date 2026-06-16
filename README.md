# Fintech HTML Dashboard Generator

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Skill: Trae](https://img.shields.io/badge/Skill-Trae-2ea44f.svg)](https://trae.ai)

> 专为金融 AI 产品专家设计的单文件 HTML 仪表板生成器。基于 Trae IDE Skill 架构，快速生成交互式数据可视化页面。

## 功能特性

- **侧边栏导航布局** - 240px 固定宽度侧边栏 + 弹性主内容区
- **ECharts 图表集成** - 支持折线图、柱状图、饼图、雷达图、双轴图等
- **智能客服浮窗** - 右下角可展开的对话窗口，支持关键词自动回复
- **金融级配色体系** - 低饱和度专业配色，6 套预设主题
- **响应式设计** - 适配 1366px - 1920px 桌面分辨率
- **PDF 导出支持** - 一键导出 PDF，支持打印样式优化
- **零依赖** - 除 ECharts CDN 外完全自包含

## 快速开始

### 安装

将此 Skill 安装到 Trae IDE：

```bash
# 克隆到 Trae skills 目录
git clone https://github.com/yourusername/fintech-html-dashboard.git ~/.trae-cn/skills/fintech-html-dashboard

# 重启 Trae IDE 即可使用
```

### 使用

在 Trae/Workbuddy/Cursor/Claudecode/…… 中触发 Skill：

```
帮我分析AIcoding市场规模和发展趋势、机会等，并且对比cursor/Qoder/workbuddy等产品
```

或

```
做一个 AI 客服产品的演示 Demo
```

### 输入参数

| 参数 | 说明 | 示例 |
|------|------|------|
| Business Background | 页面用途 | AI 客服产品分析 |
| Target Audience | 目标受众 | 产品经理、高管 |
| Expected Goal | 预期目标 | 演示汇报、数据回顾 |
| Reference Materials | 参考材料 | 数据文档、竞品资料 |
| Primary Color Scheme | 主色调 | 深蓝、青绿、藏青 |

## 项目结构

```
fintech-html-dashboard/
├── SKILL.md                    # Skill 定义文件
├── README.md                   # 项目说明
├── assets/
│   └── template.html           # HTML 模板骨架
└── references/
    ├── color-palettes.md       # 预设配色方案
    └── chart-patterns.md       # ECharts 配置模式
```

## 页面结构

```
+------------------+----------------------------------------+
|                  |                                        |
|   SIDEBAR        |        MAIN CONTENT AREA               |
|   (240px)        |        (flex: 1)                       |
|                  |                                        |
|   [Nav Item 1]   |   +-------------------------------+   |
|   [Nav Item 2]   |   |                               |   |
|   [Nav Item 3]   |   |   Page content switches       |   |
|   [Nav Item 4]   |   |   based on sidebar selection  |   |
|   ...            |   |                               |   |
|                  |   +-------------------------------+   |
|                  |                                        |
|   [By Abel]      |                                        |
+------------------+----------------------------------------+
                                            [💬 Chat Float]
```

## 图表类型

| 数据类型 | 图表 | ECharts 类型 |
|---------|------|-------------|
| 时间序列 | 折线图 | `type: 'line'` |
| 分类对比 | 柱状图 | `type: 'bar'` |
| 占比分布 | 饼图 | `type: 'pie'` |
| 多维评分 | 雷达图 | `type: 'radar'` |
| 双指标对比 | 双轴图 | 双 yAxis |

## 配色方案

- **Deep Blue** - 经典金融蓝 `#1a365d`
- **Teal** - 科技青绿 `#0d7377`
- **Navy** - 沉稳藏青 `#0f172a`
- **Emerald** - 商务翠绿 `#065f46`
- **Slate** - 现代岩灰 `#334155`
- **Indigo** - 深邃靛蓝 `#312e81`

## 适用场景

- 业务需求调研看板
- 标准化需求文档展示
- 竞品分析可视化
- 市场/行业研究仪表板
- 产品演示原型

## PDF 导出

生成 HTML 后，系统会自动调用 `mcp_Qieman_RenderHtmlToPdf` 工具转换为 PDF，提供下载链接。

页面内也支持客户端 PDF 导出：

```javascript
// 点击导出按钮触发
function exportPDF() {
  window.print();
}
```

## 技术栈

- HTML5 + CSS3 + JavaScript (ES6+)
- ECharts 5.5 (CDN)
- CSS Variables 主题系统
- Flexbox + Grid 布局

## 浏览器兼容

- Chrome 80+
- Firefox 75+
- Safari 13+
- Edge 80+

## 贡献指南

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送分支 (`git push origin feature/AmazingFeature`)
5. 创建 Pull Request

## 许可证

[MIT](LICENSE) © Abel

## 致谢

- [ECharts](https://echarts.apache.org/) - 强大的开源图表库
- [Trae](https://trae.ai/) - AI 驱动的 IDE 平台
