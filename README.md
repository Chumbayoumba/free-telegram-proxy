# 🔓 Free Telegram MTProto Proxy — fake-TLS, No Logs

> Free public MTProto proxy for Telegram. fake-TLS (looks like normal HTTPS),
> no logs, high-capacity server. Works in regions where Telegram is
> throttled or blocked.

[![Proxies](https://img.shields.io/badge/proxy-online-brightgreen)](./all_proxies.txt)
[![Type](https://img.shields.io/badge/type-fake--TLS-blue)](./all_proxies.txt)
[![Channel](https://img.shields.io/badge/Telegram-@vnespiska-26A5E4)](https://t.me/vnespiska)

## ⚡ Quick start

Tap the link on your phone — Telegram will offer to add the proxy automatically:

`tg://proxy?server=promo.vnespiska.org&port=443&secret=eef99265993307004249d0021d489786ef7461736b666c6f772e65676f722d6465762e7275`

Or open in a browser:

https://t.me/proxy?server=promo.vnespiska.org&port=443&secret=eef99265993307004249d0021d489786ef7461736b666c6f772e65676f722d6465762e7275

Or copy parameters manually:

| Field | Value |
|---|---|
| Server | `promo.vnespiska.org` |
| Port | `443` |
| Secret | `eef99265993307004249d0021d489786ef7461736b666c6f772e65676f722d6465762e7275` |
| Type | MTProto (fake-TLS / EE) |

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

- Site (RU): https://glushilok.net — free Telegram proxy + VPN, block checker
- Check what's blocked for you: https://glushilok.net/proverka/
- Guides (VLESS, Hiddify, routers): https://glushilok.net/guides/
- Site: https://vnespiska.uk
- Channel: https://t.me/vnespiska
- Bot: https://t.me/vnespiskabot
- Official MTProxy: https://github.com/TelegramMessenger/MTProxy

## 📝 License

Public proxy, provided as-is with no warranty. Use at your own discretion.
