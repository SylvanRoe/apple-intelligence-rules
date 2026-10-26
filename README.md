# Apple Intelligence & Siri 代理规则集

专为 Apple Intelligence 与 Siri 优化的分流规则集，适用于 Surge、Clash、Shadowrocket、Loon、Quantumult X、Stash 等网络代理工具。

## 规则集地址 (Raw 订阅链接)

- **主链接 (GitHub Raw)**:  
  `https://raw.githubusercontent.com/SylvanRoe/apple-intelligence-rules/main/AppleIntelligence.list`
- **备用链接 (Proxy.list 命名)**:  
  `https://raw.githubusercontent.com/SylvanRoe/apple-intelligence-rules/main/Proxy.list`
- **国内加速镜像 (jsDelivr CDN)**:  
  `https://fastly.jsdelivr.net/gh/SylvanRoe/apple-intelligence-rules@main/AppleIntelligence.list`

---

## 包含服务与域名

1. **Private Cloud Compute & Apple Intelligence 核心**:
   - `pcc.apple.com` (Apple 私有云计算 PCC)
   - `apple-magellan.com` (知识引擎及多模态推理)
   - `guzzoni.apple.com` (Siri 核心语音处理)
   - `smoot.apple.com` (Spotlight 及语义搜索)
   - `ls.apple.com` & `gspe1-ssl.ls.apple.com` (位置与辅助语义服务)
   - `gateway.apple.com` & `gateway.icloud.com`
   - `api.apple-cloudkit.com`
   - `amp-api.apps.apple.com` & `apps.mzstatic.com`

2. **Apple Private Relay (私密转送 & 边缘中继)**:
   - `apple-relay.apple.com`
   - `apple-relay.cloudflare.com`
   - `apple-relay.akamaized.net`
   - `apple-relay.fastly-edge.com`
   - `cp4.cloudflare.com`
   - `mask*.icloud.com`
   - `mask*.apple-dns.net`

3. **关键词匹配**:
   - `apple-intelligence`
   - `apple-relay`
   - `siri`

---

## 各客户端配置示例

### 1. Surge
```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/SylvanRoe/apple-intelligence-rules/main/AppleIntelligence.list,PROXY
```

### 2. Shadowrocket / Loon
```ini
[Rule]
RULE-SET,https://raw.githubusercontent.com/SylvanRoe/apple-intelligence-rules/main/AppleIntelligence.list,PROXY
```

### 3. Clash / Stash (rule-providers)
```yaml
rule-providers:
  AppleIntelligence:
    type: http
    behavior: classical
    url: "https://raw.githubusercontent.com/SylvanRoe/apple-intelligence-rules/main/AppleIntelligence.list"
    path: ./ruleset/AppleIntelligence.yaml
    interval: 86400

rules:
  - RULE-SET,AppleIntelligence,PROXY
```
