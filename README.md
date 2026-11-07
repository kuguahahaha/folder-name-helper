# folder-name-helper
📁 文件夹命名助手 - 一键生成标准化文件夹名称

🚀 V2.0.0 升级内容
✨ 核心新功能：
• 新增「日期输入框」（非必填），不再固定取系统当天
• 兼容多种日期写法智能转换：
  - 0811       → 2026-08-11（4 位自动补当前年）
  - 20260811   → 2026-08-11（8 位完整指定年月日）
  - 08-11      → 2026-08-11（分隔符自动忽略）
  - 08_11      → 2026-08-11
  - 2026-08-11 → 保持不变
  - 留空       → 取系统当天日期
• 日期合法性校验：月份 01-12，日期按实际天数校验（自动处理闰年）

✨ 交互优化：
• 页面加载后自动聚焦日期输入框（v1.0.1 聚焦时间框）
• 重置按钮清空所有三个输入框（日期、时间、项目名）

V1.0.1
✨ 视觉优化：
• 主色调升级为蓝绿渐变系，增加视觉层次
• 输入框聚焦时添加高亮边框+阴影动效
• 按钮添加 hover 渐变 + 轻微上浮效果
• 结果区域采用卡片式设计，搭配图标标识

✨ 交互增强：
• 项目名称输入框支持 Enter 键触发生成（keyCode 13）
• 新增「重置」按钮，一键清空所有输入并隐藏结果
• 时间输入框增加实时格式提示

✨ 版本说明：
• 页面底部添加折叠式「更新日志」区域（小字号，可展开）
• 显示当前版本号 + 升级内容摘要

✨ 细节打磨：
• 所有按钮添加 transition 过渡动画
• 复制成功提示改为顶部 Toast 轻提示（不阻塞操作）
• 输入框添加 ✨ 图标前缀，提升辨识度

V1.0.0
✅ 核心功能：
1. 自动获取当前日期作为文件夹名前缀（格式：YYYY-MM-DD_）
2. 支持多种时间输入格式智能转换：
   • 1416    → 14_16
   • 905     → 09_05  
   • 14_16   → 保持 14_16
3. 输入项目名称，组合生成完整文件夹名：
   • 示例：2026-03-18_14_16-项目汇报
4. 一键复制结果到剪贴板（兼容新旧浏览器）
5. 基础表单验证：
   • 项目名称不能为空
   • 时间格式校验（小时00-23，分钟00-59）

✅ 交互体验：
• 结果区域默认隐藏，生成后显示
• 复制按钮动态显示
• 输入框有 placeholder 提示

✅ 技术实现：
• 纯前端 HTML+CSS+JS，无依赖
• 响应式布局，最大宽度 650px 居中
• 使用 Microsoft YaHei 字体，适配中文环境


## 🔗 在线使用

| 入口 | 链接 |
|---|---|
| 最新版（v2.0.5） | https://kuguahahaha.github.io/folder-name-helper/ |
| 版本列表（全部历史版本） | https://kuguahahaha.github.io/folder-name-helper/versions/ |
| v2.0.5 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.5.html |
| v2.0.5 Windows 版下载 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.5.hta |
| v2.0.4 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.4.html |
| v2.0.4 Windows 版下载 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.4.hta |
| v2.0.3 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.3.html |
| v2.0.3 Windows 版下载 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.3.hta |
| v2.0.2 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.2.html |
| v2.0.1 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.1.html |
| v2.0.0 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v2.0.0.html |
| v1.0.1 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v1.0.1.html |
| v1.0.0 直达 | https://kuguahahaha.github.io/folder-name-helper/versions/v1.0.0.html |

<!-- RELEASE-NOTE-v2.0.2 -->

## 🚀 V2.0.2（2026-11-04）
• 重置按钮下方新增「常用位置」收藏栏：点击快速切换目标目录，数量不限
• 收藏跨会话保存（IndexedDB）；重复添加自动去重

## 🚀 V2.0.1（2026-10-30）
• 新增「新建文件夹」：自动校验输入、生成名称并直接在目标目录创建
• 非法字符 / 同名目录 / 路径存在性 / 写入权限提示

## 📐 V2.0.3（2026-11-05）
• 「复制结果」按钮上移：与「生成名称」同排，生成即可一键复制
• 同步更新 Windows 版 (.hta) 下载

## 🕐 V2.0.4（2026-11-05）
• 时间留空自动取当前时间：日期、时间都不填时，只填项目名称即可生成「今天 + 当前时间」的文件夹名
• 单独指定日期、时间留空时，取指定日期加当前时间

## 🧰 V2.0.5（2026-11-07）
• 修复时间固定：留空的日期/时间在点击生成那一刻实时读取，页面挂机不跨天固定
• 新增「关闭重复」（HTA）：双通道枚举资源管理器窗口，同路径保留最早一个，先列出清单再确认关闭；此电脑/桌面等虚拟目录同样参与查重
• 新增「检查更新 / 切换版本」（HTA）：读取同目录或线上 version.json，新版另存新文件并可立即启动；可列出并启动本地全部 HTA 版本
• 常用位置收藏改为同目录 favorites.json 文件持久化，换版本/重启/摆渡都保留，首次运行自动生成
• 新增根 version.json 版本清单（latest / downloadUrl / notes）
