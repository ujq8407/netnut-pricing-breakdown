# netnut pricing: all six residential tiers, the annual-billing math, and when paying per IP is the cheaper call

Most people searching netnut pricing are trying to answer one question: what do I actually pay, and does the per-gigabyte model make sense for my workload? NetNut does publish its numbers, but they're spread across product pages, and the numbers that matter for a small team are not the ones on the headline. Here's the full picture, followed by the arithmetic that decides whether a per-GB subscription or a pay-per-IP model is the better fit.

## NetNut's published residential pricing

NetNut's rotating residential plans are bandwidth-based. You commit to a monthly data allowance, and the price per gigabyte drops as that allowance grows. The same six tiers appear across NetNut's country and use-case pages:

| Plan | Monthly allowance | Monthly billing | Per GB | Annual billing (per month) | Per GB |
| --- | --- | --- | --- | --- | --- |
| Starter | 28 GB | $99 | $3.53 | $84 | $3.00 |
| Advanced | 72 GB | $249 | $3.45 | $210 | $2.93 |
| Production | 150 GB | $499 | $3.32 | $423 | $2.82 |
| Semi-Pro | 350 GB | $999 | $2.85 | $850 | $2.43 |
| Professional | 800 GB | $1,999 | $2.49 | $1,696 | $2.12 |
| Master | 2 TB | $3,750 | $1.87 | $3,180 | $1.59 |

Two notes that come directly off those pages: connections are unlimited on every tier, and NetNut adds that prices can change depending on the use case. Every plan includes city and state targeting, API access, IP whitelisting and a dedicated account manager.

Static ISP, mobile, datacenter and website-unblocker products sit on separate price sheets. Datacenter is the cheapest per gigabyte of the lot, mobile the most expensive, and the static ISP line — the one built for social accounts and long retail sessions — sits between them with a materially higher per-GB rate than rotating residential. If you came here to price a multi-account setup, the residential table above is not the number you need.

## The fine print that changes the real cost

The published table is honest, but it leaves out three things that decide whether netnut pricing works for you.

**Unused traffic doesn't roll over.** NetNut bills on a monthly subscription, and third-party reviews of the billing model note that whatever you don't burn resets at the end of the cycle. A quarterly audit or a seasonal scraping campaign therefore pays for idle months. That's a structural feature of committed-bandwidth pricing, not a NetNut quirk, but it matters when your traffic graph looks like a pulse rather than a line.

**There's no self-serve test bucket.** NetNut's own FAQ walks through the trial process: you sign up on the site, then contact the sales team by WhatsApp, Telegram, Skype, email or live chat, describe your use case and required bandwidth, and they set up a trial account. That's fine if you're procuring for a company and want a human on the other end. It's friction if you wanted to point a scraper at a target this afternoon and see what happens. Independent reviews list NetNut as having no free plan, a gated trial and a minimum entry around $99 per month.

**The floor is $99/month.** Nothing in NetNut's lineup replaces a $20 test purchase. If your monthly footprint is 10–20 GB, the Starter tier is priced at a level where most hobby and single-operator workloads simply don't belong.

None of this is a knock on the product. NetNut routes residential traffic through ISP-level infrastructure rather than peer-to-peer devices, which is why its latency and IP trust scores hold up on hard targets, and it's why the bandwidth has a real marginal cost instead of a near-zero one. The company's customers are largely enterprise teams scraping US retail and ad-verification data at volume. The pricing reflects that.

## Where the per-gigabyte model stops paying off

Run the comparison on your own numbers rather than on the marketing.

Say you're pulling 150 GB a month. NetNut's Production tier is $499 monthly, or $423 per month if you take the annual commitment. Say you're pulling 500 GB: that's between Professional and a custom quote, roughly $1,696–$1,999 a month on the annual and monthly rates respectively. At that point efficiency stops being about the per-GB rate and starts being about whether every one of those gigabytes needed an ISP-routed IP in the first place.

A lot of teams discover it didn't. Sessions that live for hours, heavy pages, video assets, large product-image pulls, dashboard work in anti-detect browsers — these consume bandwidth fast, and the per-GB meter charges for every byte regardless of how few distinct IPs the job actually needs. If your workflow burns 300 GB through 200 addresses, you're paying a traffic tax on top of the identity you wanted.

## The other billing model: pay per IP, unlimited bandwidth

9Proxy sells residential access a different way. Instead of metering traffic, its IP-based packages are one-time purchases of residential IPs with unlimited bandwidth while an IP is active, and the IPs don't expire if you haven't used them. A single IP stays alive anywhere from a few hours up to about 24 hours depending on the address, and you can generate as many endpoints as you've bought.

For the workflows above — long sessions, multi-account operations, big transfers through a small set of addresses — the cost stops scaling with page weight. Scrape 100 pages through an IP or 10,000, the invoice is the same. That's the part worth testing against your own traffic graph before you sign a monthly commitment anywhere.

The network itself is 20M+ residential IPs across 90+ countries, with HTTP(S) and SOCKS5 support, country/state/city/ZIP/ISP targeting on the bandwidth plans, and both sticky and rotating sessions. On the IP side you authenticate through the 9Proxy desktop app with local port forwarding; on the bandwidth side you use username/password or IP whitelisting straight from the dashboard, no app required. Payments run through cards, crypto, Alipay, Apple Pay and Google Pay.

If your workload is mostly rotation-heavy and light per request, bandwidth is still the right purchase — it's just bought as a prepaid bucket instead of a monthly subscription. Traffic on 9Proxy's GB plans stays valid for 180 days, and Enterprise accounts remove the expiry entirely. That kills the "use it or lose it" problem that makes monthly commitments painful for bursty projects.

## 9Proxy's current prices, in full

One thing to know before you compare these to older blog posts: 9Proxy adjusted IP-based and bundle pricing on 1 June 2026, its first change in three years. GB-based prices were left untouched. The tiers below reflect the post-adjustment rates that are publicly documented.

### IP-based packages (unlimited bandwidth, no expiry)

| Package | Effective rate | Total | Buy |
| --- | --- | --- | --- |
| 100 IPs | $0.24/IP | $24 | [ 100 residential IPs, unlimited bandwidth](https://bit.ly/9-Proxy) |
| 500 IPs | $0.144/IP | $72 | [ 500-IP package for solo operations](https://bit.ly/9-Proxy) |
| 1,000 IPs + 500 bonus | $0.084/IP | $126 | [ most popular 1,000 + 500 IP tier](https://bit.ly/9-Proxy) |
| 100,000 IPs (Business) | $0.023/IP | $2,300 | [ Business-tier IP inventory](https://bit.ly/9-Proxy) |
| 500,000 IPs (Business) | $0.018/IP | $8,625 | [ 500,000-IP wholesale package](https://bit.ly/9-Proxy) |

Per-IP cost keeps falling through the intermediate volume tiers the pricing page lists between 500 and 100,000 IPs. Those in-between tiers are where agencies usually land, so it's worth opening the pricing page rather than assuming the two ends of the range are your only options.

### Bandwidth packages (180-day validity)

| Package | Rate | Total |
| --- | --- | --- |
| 5 GB | $3.00/GB | $15 |
| 50 GB + 5 GB bonus | $2.10/GB | $105 |
| 100 GB | $1.50/GB | $150 |
| 200 GB | $1.00/GB | $200 |
| 1,000 GB | $0.80/GB | $800 |
| 2,000 GB | $0.75/GB | $1,500 |

Larger commitments scale down to $0.68/GB at the top published tier. Put that next to $3.53/GB on NetNut's smallest plan and $1.59/GB at the very top of NetNut's annual pricing, and the gap is the whole argument for this model on rotation-heavy, moderate-volume work.

### Bundle packages (IPs + traffic)

| Bundle | Contents | Price | Buy |
| --- | --- | --- | --- |
| Starter | 100 IPs + 5 GB | $30 | [ Starter bundle for small projects](https://bit.ly/9-Proxy) |
| Popular | 1,500 IPs + 50 GB | $180 | [ Popular bundle for mixed workloads](https://bit.ly/9-Proxy) |
| Pro | 5,000 IPs + 500 GB | $720 | [ Pro bundle with 500 GB of traffic](https://bit.ly/9-Proxy) |

### Enterprise

Enterprise is quoted per account. It includes unlimited data validity, a team of one owner plus up to five members sharing non-expiring bandwidth, per-member traffic limits, full activity logs, VIP pricing and dedicated support. If you're scaling past a few hundred gigabytes a month, that's the tier to price — and given NetNut's entry point sits at $99/month, it's worth getting both quotes in the same week.

A limited trial is available: 9Proxy's team has described handing out a small number of free IPs or a small bandwidth bucket to new users on request, subject to availability. Ask before you commit to a large package.

## Which model fits which job

**Take NetNut's rotating residential if** you're scraping US-heavy targets where IP trust is the bottleneck, you have a procurement process that wants a sales contact, and your monthly volume is consistently in the hundreds of gigabytes or beyond. The ISP-level architecture is the differentiator, and at 2 TB/month on annual billing the effective rate is $1.59/GB.

**Take a pay-per-IP model if** bandwidth usage is unpredictable, sessions run long, or you need hundreds to thousands of separate identities without paying for the bytes moving through them. A 1,000-IP package at $126 with no expiry covers a surprising amount of multi-account and browser-automation work.

**Take bandwidth with 180-day validity if** you rotate hard but move little data per request — SERP checks, price monitoring, geo-verification, API polling. There's no monthly reset, so an uneven project schedule doesn't cost you anything.

## Before you pay anyone

- Work out your real monthly GB from logs, not estimates. Traffic estimates in this market are routinely off by 2–3×.
- Check whether your job needs many IPs or a lot of data. They're different purchases, and most teams overbuy one of them.
- Read the expiry rules. "Unlimited" on an IP package usually means unlimited bandwidth while active, not an unlimited supply of fresh addresses.
- Test before scale. Both vendors gate the best pricing behind volume; neither wants you buying 100,000 IPs before you know your success rate on the target domains you care about.
- Confirm the payment rail you actually use, especially if you're outside the card networks' comfort zone.

## FAQ

**Is NetNut's pricing public?**
The rotating residential tiers are published on NetNut's own pages, with monthly and annual rates. Static ISP, mobile, datacenter and unblocker products are priced separately, and larger volumes go to custom quotes.

**Does NetNut have a free trial?**
Not a self-serve one. NetNut's FAQ describes signing up and then requesting a trial account from the sales team with your use case and bandwidth requirements. Several independent reviews list no free plan alongside the gated trial.

**What's the cheapest way into residential proxies?**
For small volumes, a prepaid bandwidth bucket or a small IP package. NetNut's floor is around $99/month; 9Proxy's smallest bandwidth pack is $15 and its smallest IP pack is $24.

**Do unused IPs expire?**
On 9Proxy's IP-based packages, unused IPs don't expire, and bandwidth stays valid for 180 days, or indefinitely on Enterprise. NetNut's monthly plans reset at the end of each cycle.

**Can I run both?**
Plenty of teams do — one provider for the high-trust targets that justify ISP-routed bandwidth, another for volume work where cost per request dominates. Test each on the domains you actually hit before deciding which one scales.
