# Bright Data 住宅代理

[![Promo](https://github.com/bright-cn/Rotating-Residential-Proxies/blob/main/50%25%20off%20promo%20(1).png)](https://bright.cn/proxy-types/residential-proxies) 

## 概述
体验 Bright Data 的[行业领先的住宅代理](https://bright.cn/proxy-types/residential-proxies)，提供精准的定位、卓越的稳定性和快速响应时间。

- **7200万+ 住宅IP**
- **粘性和旋转会话**
- **99.95% 成功率**
- **支持 HTTP(S) & SOCKS5**
- **地理位置定位（免费）**

## 主要特点
- **全球覆盖**：在[195个国家](https://bright.cn/locations)提供住宅代理。
- **高成功率**：在您的数据采集项目中实现高达99.95%的成功率。
- **快速响应**：平均响应时间约为0.7秒。
- **道德来源**：所有代理均获得用户明确同意。
- **无限并发会话**：无限制地扩展您的操作。

## 价格计划
- **按需付费**：$8.4/GB，无需每月承诺。
- **月度订阅**：
  - **69 GB**：$7.14/GB，$499/月。
  - **158 GB**：$6.3/GB，$999/月。
  - **339 GB**：$5.88/GB，$1999/月。
  - **企业计划**：提供满足大规模需求的定制方案。

注册并获得首次充值的1:1匹配奖励，最高达$500！

## 开始使用住宅代理
1. **开始免费试用**：无需信用卡。
2. **集成**：使用我们的API或控制面板来管理IP和配置。
3. **支持的语言**：提供Python、Java、C#、Node.js 和 Shell 的快速入门示例。

## 代码示例

### Python

```python
import sys

# 将 '[your customerID]'、'residential' 和 '[your password]' 替换为您的实际 Bright Data 客户ID、区域和密码
if sys.version_info[0] == 2:
    import six
    from six.moves.urllib import request
    opener = request.build_opener(
        request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-residential:"[your password]"@brd.superproxy.io:33335',
             'https': 'http://brd-customer-[your customerID]-zone-residential:"[your password]"@brd.superproxy.io:33335'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())

if sys.version_info[0] == 3:
    import urllib.request
    opener = urllib.request.build_opener(
        urllib.request.ProxyHandler(
            {'http': 'http://brd-customer-[your customerID]-zone-residential:"[your password]"@brd.superproxy.io:33335',
             'https': 'http://brd-customer-[your customerID]-zone-residential:"[your password]"@brd.superproxy.io:33335'}))
    print(opener.open('https://geo.brdtest.com/mygeo.json').read())
```

### Java

```java
package example;

import org.apache.http.HttpHost;
import org.apache.http.client.fluent.*;

public class Example {
    public static void main(String[] args) throws Exception {
        // 将 '[your customerID]' 和 '[your password]' 替换为您的实际凭据
        HttpHost proxy = new HttpHost("brd.superproxy.io", 33335);
        String res = Executor.newInstance()
            .auth(proxy, "brd-customer-[your customerID]-zone-residential", "[your password]")
            .execute(Request.Get("https://geo.brdtest.com/mygeo.json").viaProxy(proxy))
            .returnContent().asString();
        System.out.println(res);
    }
}
```

### C#

```c#
using System;
using System.Net;

class Example
{
    static void Main()
    {
        // 将 '[your customerID]' 和 '[your password]' 替换为您的实际凭据
        var client = new WebClient();
        client.Proxy = new WebProxy("brd.superproxy.io:33335");
        client.Proxy.Credentials = new NetworkCredential("brd-customer-[your customerID]-zone-residential", "[your password]");
        Console.WriteLine(client.DownloadString("https://geo.brdtest.com/mygeo.json"));
    }
}
```

### Node.js

```node.js
require('request-promise')({
    url: 'https://geo.brdtest.com/mygeo.json',
    proxy: 'http://brd-customer-[your customerID]-zone-residential:"[your password]"@brd.superproxy.io:33335',
})
.then(function(data){ console.log(data); },
    function(err){ console.error(err); });
```

### Shell

```shell
# 将 '[your customerID]' 和 '[your password]' 替换为您的实际凭据
curl --proxy brd.superproxy.io:33335 --proxy-user brd-customer-[your customerID]-zone-residential:[your password] -k "https://geo.brdtest.com/mygeo.json"
```

## 集成
我们的住宅代理可以与流行的工具和框架集成，包括：

- [**Puppeteer**](https://bright.cn/integration/puppeteer)
- [**Selenium**](https://bright.cn/integration/selenium)
- [**Playwright**](https://bright.cn/integration/playwright)
- [**AdsPower**](https://bright.cn/integration/adspower)
- [**MultiLogin**](https://bright.cn/integration/multilogin)

## 使用案例
了解企业如何利用住宅代理：

- [**电商**](https://bright.cn/use-cases/ecommerce)：跟踪价格和评论。
- [**社交媒体**](https://bright.cn/use-cases/social-media-for-marketing)：监控趋势。
- [**房地产**](https://bright.cn/use-cases/real-estate)：收集市场数据。
- [**旅游**](https://bright.cn/use-cases/travel)：跨地区比较价格。
- [**金融服务**](https://bright.cn/use-cases/financial)：安全地分析趋势。

## 常见问题

### 什么是住宅代理？
住宅代理提供来自真实用户的IP，使您可以像物理上位于特定位置一样收集数据。

### 住宅代理的优势是什么？
- 绕过地理位置限制
- 无被检测风险的网络爬取
- 进行市场研究和价格比较

### 有哪些计划可供选择？
Bright Data 提供灵活的定价模式，包括：

- **按需付费**：按GB计费。
- **订阅计划**：每月、每年和自定义选项。

### Bright Data 的住宅代理是否合规且安全？
Bright Data 的代理来源可靠，我们遵守所有相关的数据保护法律，包括 GDPR 和 CCPA。

### 是否提供专属支持？
我们的专属支持团队全天候提供帮助。请联系我们，讨论您的需求并最大限度地利用我们的住宅代理网络。
