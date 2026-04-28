# TeachAny Image Vault 📚🖼️

TeachAny 教学课件预制图片库。

## 架构说明

本仓库为 [TeachAny](https://github.com/weponusa/teachany) 项目的**图片资源独立仓库**，
通过 jsDelivr CDN 全球加速分发：

```
https://cdn.jsdelivr.net/gh/weponusa/teachany-images@main/{subject}/{filename}
```

### 为什么独立存储？

- **Skill 体积最小化**：TeachAny Skill 只携带 `image-registry.json` 索引文件（~50KB），
  不捆绑图片二进制文件，用户安装 Skill 时无需下载数 GB 的图片
- **CDN 加速**：jsDelivr 提供全球边缘节点缓存，任何地区用户秒级获取
- **统一质量管控**：项目维护者集中生成和管理图片，确保风格一致

### 目录结构

```
├── math/          # 数学
├── physics/       # 物理
├── biology/       # 生物
├── chemistry/     # 化学
├── history/       # 历史
├── geography/     # 地理
├── chinese/       # 语文
├── english/       # 英语
└── science/       # 科学
```

### 图片类型

| Slot | 说明 |
|:---|:---|
| `*-hero.png` | 知识结构信息图（Hero 主图） |
| `*-scene.png` | 情境/生活应用场景图 |
| `*-experiment.png` | 实验/观察场景图 |
| `*-concept.png` | 核心概念可视化图 |
| `*-abt-intro.png` | ABT 叙事框架引入图 |

## 使用方式

图片索引维护在 TeachAny 主仓库：
`skill/assets/image-registry.json`

AI 制作课件时按索引从 CDN 按需下载，不需要预先下载整个仓库。

## License

MIT
