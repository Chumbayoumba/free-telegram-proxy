# 🔓 Free Telegram MTProto Proxy — fake-TLS, No Logs

<!-- GIVEAWAY:START -->
<a href="https://t.me/vnespiskabot?start=gw_github"><img src="https://vnespiska.win/gw/img/giveaway-4x1.webp" alt="Giveaway: 3 × 90 days, 7 × 30 days of VPN, 30 × 20% discounts" width="100%"></a>

> 🎁 **Giveaway, winners drawn on 10 October at 20:00 MSK:** 3 × 90-day and 7 × 30-day VPN subscriptions, 30 × 20% discounts. Free to enter in Telegram, takes a minute: **[join →](https://t.me/vnespiskabot?start=gw_github)** · +1 ticket per invited friend
>
> 💡 Already a Geodema subscriber? Won days are added to your current plan.
<!-- GIVEAWAY:END -->

> Free public MTProto proxy for Telegram. fake-TLS (looks like normal HTTPS),
> no logs, high-capacity server. Works in regions where Telegram is
> throttled or blocked.

[![WEB Proxy](https://img.shields.io/badge/NEW-WEB%20Proxy-7c3aed?logo=telegram)](https://vnespiska.win/webproxy/)
[![Proxies](https://img.shields.io/badge/proxy-online-brightgreen)](./all_proxies.txt)
[![Type](https://img.shields.io/badge/type-fake--TLS-blue)](./all_proxies.txt)
[![Channel](https://img.shields.io/badge/Telegram-@vnespiska-26A5E4)](https://t.me/vnespiska)
[![Mirror](https://img.shields.io/badge/mirror%20(RU)-goida.win-success)](https://goida.win/)

## ⚡ Working proxies right now — checked from Russia

Tap **⚡ Connect** on a device with Telegram installed. The list is refreshed automatically every 2 hours and contains only proxies that connected from a Russian server.

<!-- UPDATED:START -->
> 🟢 **Обновлено: 06.10.2026 01:41 МСК** · рабочих прокси: **1** · каждый проверен подключением с российского сервера
<!-- UPDATED:END -->

> 🖥 **On a computer? Use our WEB proxy** (Telegram Desktop 7.1.1+): Telegram traffic looks like ordinary HTTPS, so it is harder to block. **[Connect in one click →](https://vnespiska.win/webproxy/)** · server `free.vnespiska.win` · secret `9fc8d7d1aeee614bd5fa3b760da44dd3` · type **WEB**


<!-- LIVE:START -->
| # | Сервер | Порт | Пинг из РФ | Подключить |
|---|--------|------|-----------|------------|
| 1 | `edge.turboass.live` | `443` | 🟡 89 мс | **[⚡ Подключить](https://t.me/proxy?server=edge.turboass.live&port=443&secret=ee51116f4018a2b3dfc9bda286c52afe9f656467652e747572626f6173732e6c697665)** |
<!-- LIVE:END -->

> 📢 Free proxies live for hours, not weeks. **Fresh ones every hour in the Telegram channel [@vnespiska](https://t.me/+FhRJPseOXOszZGM6)** (~4 000 subscribers), or get one instantly from the bot **[@vnespiskabot](https://t.me/vnespiskabot?start=proxy_notify_gh_en)**.
>
> 🛑 Telegram doesn't work even with a proxy (mobile internet white lists in Russia)? → **[VPN in @vnespiskabot](https://t.me/vnespiskabot?start=promo_VNESPISKA_gh_en)**: Basic plan free forever, Premium 239 ₽ with promo code `VNESPISKA`.

## 🆕 WEB proxy for Telegram Desktop — free

Since August 2026 **Telegram Desktop 7.1.1+** supports a new proxy type, **WEB**: Telegram traffic travels over plain HTTPS/WebSocket like an ordinary website, which makes it much harder to detect and block. The proxy never sees your messages, it only relays already encrypted data.

👉 **[CONNECT THE WEB PROXY](https://vnespiska.win/webproxy/)** (the button opens Telegram Desktop)

| Field | Value |
|-------|-------|
| **Type** | `WEB` |
| **Server** | `free.vnespiska.win` |
| **Secret** | `9fc8d7d1aeee614bd5fa3b760da44dd3` |
| **Client** | Telegram Desktop 7.1.1+ (Windows, macOS, Linux) |

Link for Telegram Desktop (paste it into Saved Messages and click it there):

```
tg://webproxy?server=free.vnespiska.win&secret=9fc8d7d1aeee614bd5fa3b760da44dd3
```

> ⚠️ Do not open `t.me/webproxy?…` in a browser: t.me does not know this link type yet and shows an unrelated channel. Stable mobile apps do not support WEB proxies yet (only Telegram beta builds do), use the MTProto proxy above.

---

## 📋 What's inside

- [`all_proxies.txt`](./all_proxies.txt) — proxy link in standard Telegram format
- [`README.md`](./README.md) — this file

## 🌍 Why MTProto over a VPN

| Feature | MTProto | VPN |
|---|---|---|
| Affects | Telegram only | All traffic |
| Speed | 90–100% native | 50–80% native |
| DPI evasion | fake-TLS (looks like HTTPS) | often obvious |
| Setup | 1 tap | install an app |
| Cost | Free | Often paid |

## 📡 Sponsor channel

This proxy has a sponsor channel attached: [@vnespiska](https://t.me/vnespiska).
That's how MTProto works in Telegram — a proxy owner can pin one channel that
appears in users' chat list while connected. Telegram explicitly labels it as a
sponsored channel. You can ignore it; to remove it, just disconnect the proxy.
The channel posts proxy updates, new servers and bypass tips. No spam.

## ❓ FAQ

**Is it safe?** The proxy only relays already-encrypted Telegram traffic, like
any router on the path. It cannot read your messages — encryption is handled by
Telegram's servers with your client's keys.

**Are logs kept?** No logs are stored on this proxy. For highly sensitive
workflows, run your own (see below).

**Why free?** The sponsor-channel mechanism grows the channel organically. The
marginal cost of extra users on a capable VPS is near zero.

**How do I check what's blocked at my ISP?** Run a free in-browser block test
(Cheburnet Connect): https://glushilok.net/proverka/ — it shows which services
are unreachable on your network and whether DPI/TSPU is present.

## 🛠 Run your own (5 min on any VPS)

```bash
git clone https://github.com/TelegramMessenger/MTProxy
cd MTProxy && make
cd objs/bin
curl -s https://core.telegram.org/getProxySecret -o proxy-secret
curl -s https://core.telegram.org/getProxyConfig -o proxy-multi.conf
SECRET=$(head -c 16 /dev/urandom | xxd -ps)
./mtproto-proxy -u nobody -p 8888 -H 443 -S $SECRET \
  --aes-pwd proxy-secret proxy-multi.conf -M 1
```

## 🤝 Want to share?

Star this repo, share the proxy link, or post it on your channel — that's how
the network grows.

## 🔗 Links

- Mirror not blocked in Russia: https://goida.win — Telegram proxy + VPN, whitelist bypass (RU)
- Site (RU): https://glushilok.net — free Telegram proxy + VPN, block checker
- Check what's blocked for you: https://glushilok.net/proverka/
- Guides (VLESS, Hiddify, routers): https://glushilok.net/guides/
- Site: https://vnespiska.win
- Channel: https://t.me/vnespiska
- Bot: https://t.me/vnespiskabot
- Official MTProxy: https://github.com/TelegramMessenger/MTProxy

## 📝 License

Public proxy, provided as-is with no warranty. Use at your own discretion.
