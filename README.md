# UESTC-CourseReport-Template (基于 DissertationUESTC 的精简课程报告模板)

> 仅保留 coursereport 模式，便于课程报告/课程设计报告快速上手。

- 仓库描述：精简自上游 UESTC 学位论文模板，仅保留并默认启用 `coursereport` 模式，聚焦课程报告场景；在不影响编译链的前提下，裁剪博士/硕士/本科/双学位分支与相关样式。支持自定义封面字段与页眉文案。
- 上游项目：基于并致谢 [MGG1996/DissertationUESTC](https://github.com/MGG1996/DissertationUESTC)

## 特性
- 仅保留 `coursereport` 模式，`\documentclass[]{DissertUESTC}` 即可生效（已在类文件中将默认选项切换为 `coursereport`）
- 提供封面自定义接口：`\SetCourseTitle{}`、`\coursecovercustom`、`\CourseCoverLine`、`\CourseCoverLineTwo`、`\CourseCoverSchoolLine`
- 统一封面大标题与页眉默认文案，开箱即用

## 目录结构（最小发布集）
```
DissertUESTC.cls        # 文档类（默认 coursereport 模式）
DissertUESTC.bst        # 参考文献样式（随模板使用）
报告模板.tex             # 课程报告示例/模板入口（可直接编译）
```

> 若需图片与字体，请按需拷贝 `fig/` 与 `font/`；本模板已内置常用字体路径配置，保持目录同名即可。

## 快速开始
1) 安装 TeX 发行版（推荐 TeXLive/MacTeX 2024 及以上）
2) 使用 XeLaTeX 编译（TeXstudio 可在首行使用 `% !TEX Program = xelatex`，VSCode/Overleaf 请手动设置）
3) 直接编译根目录中的 `报告模板.tex`

## 封面定制（示例）
在导言区可直接重定义以下命令：
```tex
\renewcommand{\CourseReportZhName}{课程报告}
\renewcommand{\CourseReportEnName}{COURSE REPORT}
\renewcommand{\CourseReportHeader}{电子科技大学课程报告}
\renewcommand{\covertitlelabel}{报告题目}
\SetCourseTitle{具体报告题目}

% 封面下方信息区（按需增删）
\renewcommand{\coursecovercustom}{%
  \CourseCoverLine{课程名称}{示例课程}
  \CourseCoverLineTwo{组}{号}{第01组}
  % \CourseCoverLine{学号}{2025XXXXXX}  % 可留空/模糊化
  \CourseCoverLine{小组成员}{张三、李四、王五}
  \CourseCoverLine{课程教师}{某某老师}
  % \CourseCoverSchoolLine[par]{某某学院}
}
```

## 文献与引用
- 参考文献数据库请置于 `ref.bib`，在文末使用：
```tex
\bibliography{ref}
```
- `.bst` 已随模板提供；学位类型差异已在上游模板中完整实现，此精简模板保留其常用能力。

## 与上游差异
- 删除：`bachelor / doublebachelor / master / promaster / intmaster / ipmaster / doctor / prodoctor / intdoctor / ipdoctor` 等选项及相关样式分支
- 保留并默认启用：`coursereport`
- 增强：课程报告封面的自定义占位与中文注释，降低上手成本

> 上游完整说明、规范细节及更新日志见：[MGG1996/DissertationUESTC](https://github.com/MGG1996/DissertationUESTC)

## 兼容性
- 推荐 TeXLive/MacTeX 2024 及以上版本
- 默认引擎：XeLaTeX

## 许可与致谢
- 本仓库基于并致谢上游项目 [MGG1996/DissertationUESTC](https://github.com/MGG1996/DissertationUESTC)
- 许可证请遵循上游项目的许可条款；如需二次分发或商用，请阅读并遵守上游许可

---

如有问题或建议，欢迎提 Issue/PR。

