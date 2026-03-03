---
summary: "WeCom (企业微信) channel plugin"
---

# WeCom (企业微信) (plugin)

This channel integrates Clawdbot with WeCom (企业微信) internal apps.

## Personal WeChat bridge (个人微信桥接)

This plugin talks to **WeCom internal apps only**. Personal WeChat access relies on the WeCom **WeChat plugin**:

1. Enable API callbacks on your WeCom app (URL points to this plugin).
2. In WeCom Admin → **My Enterprise → WeChat Plugin**, bind your personal WeChat by scanning the QR code.
3. Open the WeCom app from the WeChat plugin entry; messages are delivered to WeCom callbacks.
4. The plugin forwards messages to OpenClaw and sends replies back via WeCom APIs.

## Status

- Webhook verification: supported (requires Token + EncodingAESKey)
- Inbound messages: WIP
- Outbound: text supported; media/markdown WIP

## Callback URL

Recommended:

- `https://<your-domain>/wecom/callback`

## Security

Store secrets in environment variables or secret files. Do not commit them.
