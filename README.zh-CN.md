# Anywhere Rules

适用于 [Anywhere](https://github.com/NodePassProject/Anywhere) 的规则库，基于公开规则源转换为可导入的 `.arrs` 和 `.amrs` 文件。

[English](README.md)

## 关于 Anywhere

[Anywhere](https://github.com/NodePassProject/Anywhere) 是一款完全基于 Swift 开发的原生零依赖代理客户端。无 Electron，无 WebView，非 sing-box 壳程序。从底层实现纯协议封装，支持 vless、trojan、hysteria、shadowsocks、http 等多种主流协议，同时兼顾稳定与性能。

## 内容

- `rules/common/`：常用路由规则集。
- `rules/all/`：全量转换路由规则集。
- `mitm/`：实验性 MITM 规则集及相关 Reject 规则集。

## 使用

### 路由规则

在 Anywhere 中导入 `.arrs` 链接。

```text
https://raw.githubusercontent.com/chikacya/anywhere-rules/main/rules/common/AI.arrs
```

导入后可将规则集分配给 `DIRECT`、`REJECT` 或代理策略。

### MITM 规则

MITM 规则为实验性内容，仅供学习交流。

将 `.amrs` 文件导入 Anywhere 的 MITM 规则集。部分 MITM 规则还需要搭配 Reject 规则，例如将 `mitm/DomainReject.arrs` 作为路由规则集导入，并分配给 `REJECT`。

请只在你有权检查的流量上启用 MITM。

## 更新

GitHub Actions 每天自动更新生成规则。

## 说明

Anywhere 路由规则集当前支持域名后缀、域名关键词、IPv4 CIDR 和 IPv6 CIDR。上游中无法等价表达的规则类型会在转换时跳过。

## 致谢

感谢以下公开规则与脚本项目/作者的长期维护：

- blackmatrix7/ios_rule_script
- ACL4SSR/ACL4SSR
- SukkaW/Surge
- ConnersHua/RuleGo
- NobyDa/Script
- Loyalsoldier/v2ray-rules-dat
- Loyalsoldier/surge-rules
- TG-Twilight/AWAvenue-Ads-Rule
- limbopro/Adblock4limbo
- dler-io/Rules
- geekdada/surge-list
- fmz200/wool_scripts
- VirgilClyne/iRingo
- app2smile/rules
- luestr/ProxyResource
- 等
