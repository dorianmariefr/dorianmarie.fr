---
layout: default
title: Adding a rate-limiting section to thoughtbot's guides
date: 2022-05-22 17:04 +0200
---

I was reading [thoughtbot's guides](https://github.com/thoughtbot/guides) just
before joining thoughtbot when I noticed the security page was missing a section
about rate-limiting.

### Why was this change necessary?

People reading this guide might feel like they have a pretty secure application
after reading the guide.

But those applications could be vulnerable to:

- bots trying many email/password combinations (credentials stuffing, brute force attacks);
- bots uploading a lot of links in comments (spam);
- bots hitting slow endpoint to exhaust resources ((Distributed) Denial of Service)
- etc.

### How does it address the problem?

Rate-limiting limits those kinds of attacks by limiting the number of requests
per time frame that clients make to a set of endpoints.

It can be:

- limiting to creating an user every hour by IP address;
- limiting to 100 requests per minute to API endpoints by user ID;
- etc.

### Are there any side effects?

Real users can be blocked and need to wait before retrying.

Also having a proper error message to indicate to the user that they can retry
in X minutes/hours helps keep users not frustrated.

## See it live

You can find the result as of the time of writing on
[github.com/thoughtbot/guides/security/application.md#rate-limiting](https://github.com/thoughtbot/guides/blob/4ee4db025ea836a558b70fd5acf69b691b87022d/security/application.md#rate-limiting).

> ## Rate-limiting
>
> An attacker could try many passwords, OTP codes, emails, or any kind of input
> to compromise your system.
>
> An attacker could also request slow endpoints of your application to make it
use its limited-resources.
>
> Tools like [rack-attack](https://github.com/rack/rack-attack) can help you
minimize this attack surface.
