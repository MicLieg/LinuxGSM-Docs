# Rocket.Chat

![Rocket.Chat Logo](../.gitbook/assets/rocket.chat.jpg)

[Rocket.chat](https://www.rocket.chat/) is an open-source collaboration tool.

## Create a Rocket.chat Webhook

1. Follow the [Rocket.chat guide](https://docs.rocket.chat/guides/administrator-guides/integrations#incoming-webhook-script) on how to create an incoming webhook.
2. Copy the Webhook URL.
3. Turn on Rocket.chat alerts and copy the Webhook URL into the [LinuxGSM settings](../configuration/linuxgsm-config.md).

```bash
# Rocket.Chat Alerts | https://docs.linuxgsm.com/alerts/rocket.chat
rocketchatalert="off"
rocketchatwebhook="webhook"
```
