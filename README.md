# KISS Translator 订阅规则

维护者：Rowan-memoedu。唯一维护入口是本仓库的 `kiss-rules_v2.json`。

## 订阅地址

https://raw.githubusercontent.com/Rowan-memoedu/kiss-translator-rules/main/kiss-rules_v2.json

在 KISS 设置 → 网页翻译 → 订阅规则中添加此地址，选中它，开启「注入订阅规则」，刷新订阅缓存。

本订阅包含 Math Academy、Hyperskill 两条维护规则，以及原来启用的 18 条社区规则快照。KISS 2.1.0 一次只选中一个订阅，因此把原社区规则保留在同一个文件中。社区规则是快照，不会自动跟随上游更新。

## 作者自己的迁移步骤

先选中并刷新本订阅，确认列表内出现 Math Academy、Hyperskill，再删除「个人规则」中的 `www.mathacademy.com`、`hyperskill.org` 两条。删除后重新打开网页，核对翻译。个人站点规则应为空，以后只修改本仓库并推送，再刷新订阅缓存。

本地全局规则仍作兜底：KISS 2.1.0 会过滤订阅文件中的 `pattern: "*"`，无法仅通过订阅迁移全局规则。两条维护规则已展开作者当前的全局继承值，避免它们因订阅者的全局设置不同而改变元素选择和显示模式。

## 服务与范围

两条维护规则引用名为 `DeepSeek` 的翻译服务，并使用仅译文模式。订阅者需要自行配置可用的 DeepSeek 服务；本仓库不包含密钥、服务连接配置、个人提示词、Cookie 或其他浏览器数据。规则相同不能保证不同模型和提示词产生完全相同的译文。

Math Academy 保留现有课程页选择器、公式保护和关闭自动扫描的行为。它仍覆盖整个 `www.mathacademy.com` 域名，但并非所有非课程页面都能命中选择器；此次迁移不扩大翻译范围。

## 更新

直接编辑 `kiss-rules_v2.json` 并提交到 `main`。订阅者刷新订阅规则后取得更新。请勿通过个人规则覆写同一网站，否则会遮盖本订阅的更新。

## 来源与许可

18 条社区规则来自作者在 2026-10-11 启用的 [fishjar/kiss-rules](https://github.com/fishjar/kiss-rules) 缓存快照，遵循 MIT 许可；原许可见 `LICENSE`。KISS 的订阅格式和优先级参考 [官方项目](https://github.com/fishjar/kiss-translator)。
