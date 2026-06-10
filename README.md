# Anywhere Rules

Rule sets for [Anywhere](https://github.com/NodePassProject/Anywhere), converted from public rule sources into importable `.arrs` and `.amrs` files.

[简体中文](README.zh-CN.md)

## About Anywhere

[Anywhere](https://github.com/NodePassProject/Anywhere) is a native proxy client built entirely with Swift. It has no Electron, no WebView, and is not a sing-box wrapper. It implements protocols directly from the lower layers, supports vless, trojan, hysteria, shadowsocks, http, and other mainstream protocols, and focuses on stability and performance.

## Contents

- `rules/common/` - curated routing rule sets for daily use.
- `rules/all/` - full converted routing rule sets.
- `mitm/` - experimental MITM rule sets and related reject rule sets.

## Usage

### Routing Rules

Import a `.arrs` URL in Anywhere.

```text
https://raw.githubusercontent.com/chikacya/anywhere-rules/main/rules/common/AI.arrs
```

Use the imported rule set with `DIRECT`, `REJECT`, or your preferred proxy policy.

### MITM Rules

MITM rules are experimental and are provided for learning and research only.

Import `.amrs` files into Anywhere MITM rule sets. Some MITM rules also need a matching reject rule set, such as `mitm/DomainReject.arrs`, imported as a routing rule set and assigned to `REJECT`.

Only enable MITM for traffic you are allowed to inspect.

## Update

GitHub Actions updates generated rules daily.

## Notes

Anywhere routing rule sets currently support domain suffix, domain keyword, IPv4 CIDR, and IPv6 CIDR. Unsupported upstream rule types are skipped during conversion.

## Thanks

Thanks to the upstream projects and authors who maintain public rules and scripts:

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
- and more
