---
{"dg-publish":true,"permalink":"/not-masking-wp-login/"}
---

Masking the WordPress login page (changing its default URL, /wp-login.php) was once considered a helpful Wordpress security practice. However, it is no longer recommended[^1]. Modern security approaches provide more robust and sustainable protection without the complications that masking introduces. Leveraging tools like Cloudflare’s Web Application Firewall (WAF) rules provides far more robust protection without introducing the downsides of masking the login path.
## Why We No Longer Recommend Masking wp-login
1. Security through obscurity is ineffective 
	1. Masking the login URL doesn’t prevent determined attackers. Tools like scanners and bots can still locate login forms by analyzing site patterns or JavaScript.
2. Maintenance overhead
	1. Some compatibility issues with third-party tools[^2] and services.
	2. Team members and clients often struggle to remember or bookmark the custom login path.
3. Limited efficiency against bots
	1. Many automated bots and targeted attackers can still locate and exploit login forms, even with custom URLs, by brute-forcing or using advanced scanning techniques.
4. Better alternatives exist
	1. Cloudflare rules[^3]


# Footnotes

[^1]: https://chriswiegman.com/2021/10/please-stop-hiding-wp-admin/
[^2]: [Know plugin conflicts](https://apps.wordpress.com/support/mobile/login-signup/known-plugin-conflicts/?utm_source=chatgpt.com), [Defender Pro issues](https://wordpress.org/support/topic/masking-url-login-causing-registration-problem/?utm_source=chatgpt.com), [Mobile app issues](https://apps.wordpress.com/support/mobile/login-signup/known-plugin-conflicts/), [Registration issues](https://wordpress.org/support/topic/masking-url-login-causing-registration-problem/?utm_source=chatgpt.com)
[^3]: [Cloudflare WAF Rules V3 by Web Agency Hero](https://webagencyhero.com/cloudflare-waf-rules-v3/)