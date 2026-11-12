# codex 计划

## 根据代码改动更新 CHANGELOG.rst

```
 请根据上一版本发布以来的 Git 代码变更，更新 `CHANGELOG.rst`。  
 在文件顶部新增下一版本的更新记录 请先查看相关提交记录和代码差异，确保内容准确，不要虚构变更。保留已有历史记录，不修改旧版本内容，并沿用项目现有的版本命名和文档格式。
```

## 配置control版本

```
现在创建deb之前。需要
sed -i 's/^Version:.*/Version: 0.2.6/' debian/control
改成control直接读取~/Tool/code-version-manager/VERSION，版本还是保留0.2.6,在~/Tool/code-version-manager/CHANGELOG.rst补充更新内容就行
```

## 编写项目AGENTS.md文件

```
通读当前项目，把你学到的关于项目的信息保存到AGENTS.md文件里。用中文，格式要清晰
```

## 配置格式由项目现有构建方式决定

```
配置格式由项目现有构建方式决定：
请将更新仓库放入项目的构建配置，在发布软件时确定，默认使用 `lqxmb/code-version-manager`。
请先检查项目现有构建流程，优先复用已有配置。配置格式应与项目技术栈匹配，可采用 `build_config.json`、`build_config.cmake` 或已有的等效配置，保持更新仓库只有一处配置来源。
 完成后请说明：配置文件的具体路径、配置项名称，以及发布前如何修改并让配置随构建生效。
当前项目使用 **Python + Makefile**，适合继续使用 [build_config.json]，使用 CMake 的项目可以选择 `build_config.cmake`。
```

## 地址写在构建配置里，发布软件时确定

```
地址写在构建配置里，发布软件时确定。固定使用地址。设置窗口保留“每日自动检查更新”，仓库地址可以只读展示。告诉我构建配置在哪里
```

## Dock收藏图标

```
从桌面打开后，Dock 显示正确图标和名称，右键可添加到收藏夹
```

## 转为纯ros2

```
转为纯ros2，不要残留ros1的内容, 只改动ros2的api相关部分
```
