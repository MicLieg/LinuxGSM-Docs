# Alerts

LinuxGSM allows alerts to be received using various methods, should the game server require your attention.

## Alert Settings

Alert settings can be changed in [LinuxGSM config](../configuration/linuxgsm-config.md)

### More Info

Many alerts, except email only give very basic info. More info allows you to get further info about an alert using [termbin.com](https://termbin.com/). Enabling this will include all the data by adding a link to a termbin text file. These files will be kept for 7 days before being deleted.

```bash
# More info | https://docs.linuxgsm.com/alerts#more-info
postalert="off"
```

### Display IP

The IP address you want to be displayed in alerts.

By default, the LinuxGSM alert will display the external internet facing IP. Failing this will fall back to the server IP. If the IP is incorrect or you want users using a DynDNS you can change it manually by using:

```bash
# Display IP | https://docs.linuxgsm.com/alerts#display-ip
displayip=""
```
