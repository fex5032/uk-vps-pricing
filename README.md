# UK VPS pricing: what £2–£17 a month buys, when 4 vCPU is overkill, and the renewal and upgrade traps the price pages leave out

Entry-level UK VPS plans run from £2 a month to £17.34 ex. VAT, and very little of that gap comes down to CPU speed. It's whether the number you saw is a three-month teaser or a standing rate, whether backups are included or billed per gigabyte, and whether you can move up a plan without rebuilding the server. This guide works through each provider's own price page, keeps promotional rates separate from list rates, and finishes with the JustHost line-up for readers who want the most RAM and NVMe per dollar.

> **Quick pick:** if you're comparing on specs per dollar and you're comfortable in a Linux shell, JustHost's NVMe range runs from $1.99/month (512 MB) to $18.30/month (4 cores, 4 GB RAM, 120 GB NVMe), with roughly 20% off when you pay for 12 months. Prices are in USD and the plan pages don't name the datacentre, so confirm location and the sterling total with support before you pay. 👉 [Compare JustHost's current VPS plans and prices](https://justhost.asia/en/services/vps/tariffs-all?ref=196392)

## What a UK VPS actually buys you

Four things, and only one of them is about hardware.

**Latency.** A London datacentre answers a Manchester or Bristol visitor in a fraction of the round-trip time a US-hosted server adds. On a static page you won't notice. On WordPress with a database and no full-page cache, you will, because every uncached request makes that round trip several times.

**IP geolocation.** OVHcloud's own UK VPS page argues that server location and IP geolocation feed into Google ranking and that visitors are more likely to click a locally based site. Treat that as the vendor making its case rather than a measured result; the latency half of the argument is not in dispute, the ranking half is harder to pin down. What is concrete: a UK IP is what UK-only services check when they geo-block.

**Sterling billing is not the same thing as a UK server.** Contabo quotes euros, JustHost quotes dollars, OVHcloud and Fasthosts quote pounds with and without VAT. Paying in USD or EUR with a UK card usually adds a conversion margin on top of the advertised price, so a $18.30 plan isn't £18.30.

**Where the data sits.** If you handle customer records, the datacentre country is the thing your privacy notice has to match.

## JustHost's VPS line: the specs-per-dollar view

JustHost sells KVM VPS on its own site, priced in USD, with NVMe storage and "unmetered" ports that the price page describes as fair-share, alongside an equivalent monthly transfer figure. Plans carry star names rather than tiers, which makes the ladder harder to read at a glance than it needs to be.

| Plan | Specs | Monthly | 12-month rate | Order |
| --- | --- | --- | --- | --- |
| VPS Promo | 1 core · 512 MB · 5 GB NVMe · 10 Mbps | $1.99 | not shown | [Order](https://justhost.asia/en/services/vps/tariffs/promo-c1r512nvme?ref=196392) |
| New Star | 1 core · 1 GB · 10 GB NVMe · 100 Mbps | $3.81 | $3.05 | [Order](https://justhost.asia/en/services/vps/tariffs/new-star-c1r1024nvme?ref=196392) |
| Sirius | 1 core · 1 GB · 20 GB NVMe · 300 Mbps | $4.85 | $3.88 | [Order](https://justhost.asia/en/services/vps/tariffs/sirius?ref=196392) |
| Arcturus | 1 core · 2 GB · 30 GB NVMe · 300 Mbps | $6.92 | $5.53 | [Order](https://justhost.asia/en/services/vps/tariffs/arcturus?ref=196392) |
| Double Star | 2 cores · 2 GB · 20 GB NVMe · 200 Mbps | $7.08 | $5.67 | [Order](https://justhost.asia/en/services/vps/tariffs/double-star-c2r2048nvme?ref=196392) |
| Alpha Centauri | 2 cores · 2 GB · 40 GB NVMe · 400 Mbps | $8.99 | $7.19 | [Order](https://justhost.asia/en/services/vps/tariffs/alpha_centauri?ref=196392) |
| Bright Star | 4 cores · 4 GB · 30 GB NVMe · 300 Mbps | $9.80 | $7.84 | [Order](https://justhost.asia/en/services/vps/tariffs/bright-star-c4r4096nvme?ref=196392) |
| Vega | 2 cores · 4 GB · 80 GB NVMe · 500 Mbps | $13.44 | $10.75 | [Order](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392) |
| Capella | 4 cores · 4 GB · 120 GB NVMe · 750 Mbps | $18.30 | $14.64 | [Order](https://justhost.asia/en/services/vps/tariffs/capella?ref=196392) |

Two things about that table matter more than the numbers.

The 12-month column is the same plan at 80% of the monthly rate. That's a discount for committing, not a separate product, and it's the rate you should budget against if you intend to stay a year.

The VPS landing page also runs a "special offers" list that prices several of the same names lower: Sirius at $2.81/month ($2.25 on 12 months), Arcturus at $4.01 ($3.21), Vega at $7.79 ($6.23), plus three larger configurations that don't appear on the price list at all, Yildun (4 cores, 8 GB, 200 GB NVMe) at $16.20 ($12.96), Betelgeuse (6 cores, 12 GB) at $26.40 ($21.12) and Altair (8 cores, 24 GB, 600 GB NVMe) at $47.40 ($37.92). Same plan names, two different prices on the same website. Compare both pages at checkout rather than assuming the first number you saw is the one you'll be charged.

Storage type is a separate choice, and it changes the price. At the small end, a 512 MB / 5 GB server costs $2.60 on 12-month terms with HDD, $3.12 with SSD and $3.38 with NVMe. Paying for a spinning disk in 2026 to save 78 cents is a false economy on a database box, but it's fine for backups. IPv6-only instances start lower again, from $1.60, which is only useful if everything reaching your server is IPv6-capable. 👉 [See JustHost's current VPS offers and plan list](https://justhost.asia/en/vps?ref=196392)

### Does JustHost have a UK location?

Its own price pages don't say. Third-party reviews published in May 2026 describe London nodes labelled LON1 and LON2, and they disagree on an important detail: the LON1 review reports a native UK IP, while the LON2 review reports a US IP with UK service access working anyway. If a UK IP matters to you for geolocation, geo-blocked content or a UK-facing store, ask support which location and which IP range you'll get before you order. That's a two-minute chat that decides whether the plan is right for you at all.

## The UK market benchmark, with the pricing basis attached

This is where most comparisons go wrong: a "£2 VPS" and a "£17 VPS" are often not the same kind of number.

| Provider & plan | vCPU / RAM | Storage | Port | Price and basis |
| --- | --- | --- | --- | --- |
| OVHcloud VPS-1 | 2 / 4 GB | 40 GB NVMe | 500 Mbps, unlimited | £3.31 ex. VAT (£3.97 inc.), standing rate |
| OVHcloud VPS-2 | 4 / 8 GB | 75 GB NVMe | 1 Gbps | £6.29 ex. VAT (£7.55 inc.) |
| OVHcloud VPS-3 | 6 / 12 GB | 100 GB NVMe | 2 Gbps | £9.01 ex. VAT (£10.81 inc.) |
| OVHcloud VPS-4 | 8 / 24 GB | 200 GB NVMe | 3 Gbps | £17.34 ex. VAT (£20.81 inc.) |
| Contabo CLOUD VPS 4 | 4 / 8 GB | 100 GB SSD | 200 Mbit | €4.40/mo for 24 months, then €5.50 |
| Contabo CLOUD VPS 6 | 6 / 12 GB | 200 GB SSD or 100 GB NVMe | 300 Mbit | €6.00, then €7.50 |
| Contabo CLOUD VPS 8 | 8 / 24 GB | 300 GB SSD or 150 GB NVMe | 800 Mbit | €11.20, then €14.00 |
| Contabo CLOUD VPS 12 | 12 / 48 GB | 400 GB SSD or 200 GB NVMe | 800 Mbit | €20.00, then €25.00 |
| Contabo CLOUD VPS 18 | 18 / 96 GB | 600 GB SSD or 300 GB NVMe | 1 Gbit | €39.20, then €49.00 |
| IONOS VPS (entry tier) | varies by plan | NVMe | up to 1 Gbit/s external | from £2/mo, term not stated |
| Fasthosts VPS 1 | 1 / 2 GB | 60 GB NVMe | 1 Gbit | £2/mo for 3 months, then £5 |
| Fasthosts RAM VPS 16 | 16 / 64 GB | 960 GB NVMe | 1 Gbit | £48 for 3 months, then £97 |

Read the last column before the price. Fasthosts' £2 is a 90-day rate on a £5 plan, and its £97 flagship is quoted after new-customer discounts end, which is refreshingly honest and rare. Contabo's figures are a 24-month introductory price; month 25 reverts to the higher number, and those plans are in euros even though Contabo accepts sterling. OVHcloud's numbers are standing list prices with both VAT treatments shown, which is why they look more expensive than a £2 headline. IONOS's "from £2" is a starting point on a page whose plan table didn't load in my capture, so treat the number as a floor and check the configuration before comparing it to anything.

Bandwidth also isn't one thing. OVHcloud's UK plans are unlimited, with the exception of its Asia-Pacific locations, where VPS-1 gets 500 GB a month, VPS-2 and VPS-3 get 1 TB, VPS-4 gets 3 TB, and anything over that is throttled to 10 Mbps. Contabo's ports run 200 Mbit/s to 1 Gbit/s under a fair-usage policy. IONOS advertises "up to 1 Gbit/s" for external connections without promising the port.

## Which plan fits which job

**One brochure site or a blog with caching:** 1 to 2 GB RAM and 1 core is enough. That's JustHost New Star at $3.05, or OVHcloud VPS-1 at £3.31 ex. VAT with daily backups included.

**Three or four WordPress installs plus a database and a staging copy:** start at 2 cores / 4 GB, which is Vega on JustHost at $10.75 or OVHcloud VPS-2 at £6.29 ex. VAT. Below that you'll spend your evenings tuning MySQL.

**WooCommerce with real traffic spikes:** 8 vCPU / 24 GB plus included daily backups. OVHcloud VPS-4 at £17.34 ex. VAT includes those backups; JustHost Altair at $37.92 doesn't advertise a backup service, so budget for your own snapshot routine.

**Anything needing Windows, Plesk or cPanel:** check the licence line before the spec line. IONOS charges £5/month for Plesk Obsidian and requires at least 20 GB of storage on Linux or 32 GB on Windows, so a 30 GB plan leaves you very little room. Fasthosts sells Plesk Web Host Edition at £5/month too, and bundles the Windows licence into the plan price, which makes its Windows VPS slightly more expensive than the Linux equivalent but avoids a separate licence.

## What the plan tables don't tell you

**Upgrades are easier than downgrades.** OVHcloud advertises one-click in-place upgrades from the control panel, but only within the same datacentre. Dropping to a smaller plan means ordering a new server, migrating and cancelling the old one. Size for the next twelve months, not the next two weeks.

**"Local Zone" plans are cut down.** OVHcloud's Local Zone VPS doesn't support preinstalled apps, Windows, additional storage, monitoring, additional IPs, load balancers or managed databases, and it's Linux only, with Plesk, cPanel and Docker unsupported. If you picked a location for latency and assumed the full feature set came with it, you'll find out at install time.

**Backups mean different things.** OVHcloud includes a daily backup covering the previous 24 hours. Contabo gives you one to three snapshots, which is a manual rollback point, not a schedule. IONOS charges Cloud Backup from £0.045 per GB per month excluding VAT. JustHost's plan pages don't advertise backups at all, so assume you're building your own.

**Extra IPs are a line item.** IONOS charges £5 ex. VAT for each additional IPv4 beyond the one included. If you run separate SSL sites on separate IPs, that adds up faster than the server does.

**Cancellation notice is contractual.** Contabo's prepaid contracts have no minimum notice period, but post-paid ones require four weeks. Set a calendar reminder or you'll pay for a quarter you don't use.

## FAQ

**Do you need a UK datacentre if your customers are in the UK?** If your site is dynamic, yes, it's the cheapest latency win available. If you're serving a global audience from a CDN and the origin only talks to the CDN, location matters much less.

**What can a $2 or £2 plan actually run?** A 512 MB to 1 GB box handles a static site, a cached WordPress with a light plugin set, a WireGuard node, or uptime monitoring. It will not handle WooCommerce, a control panel, or a database under concurrent writes.

**What happens when the promotional price ends?** Fasthosts goes from £2 to £5 after three months. Contabo goes from €4.40 to €5.50 after 24 months. Budget the post-promotion rate into your numbers, not the teaser.

**Can you upgrade without migrating?** On OVHcloud, yes, within the same datacentre. On JustHost and Contabo, upgrades are generally a plan change, but confirm the process with support before you build anything you'd hate to rebuild.

**Is a UK IP guaranteed?** Not by any of these pages. It's the one item worth getting in writing from support, particularly if you're geolocating for search or unlocking UK-only services.

## Before you order

Match the plan to the workload, not to the discount. A single site with caching runs fine on 1 to 2 GB; a stack of WordPress installs plus a database wants 2 cores and 4 GB; a shop with campaign spikes wants 8 vCPU and 24 GB with a backup schedule you've actually tested. JustHost's Vega plan sits at the useful middle of that range: 2 cores, 4 GB RAM, 80 GB NVMe and a 500 Mbps fair-share port for $10.75 a month on a 12-month term.

Then confirm two things at checkout: whether the price you're looking at is promotional or standing, and whether backups and the IP you need are inside that price or added afterwards. Those two questions account for most of the difference between the cheapest quote and the final invoice.

👉 [Open the JustHost Vega plan and check the current 12-month price](https://justhost.asia/en/services/vps/tariffs/vega?ref=196392)
