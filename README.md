# 🚀 Chartink Bot

PHP based Webhook for sending Chartink Scan Alerts to Telegram.<br>

## About:

Live scan alerts on [Chartink](https://chartink.com/screeners) have a webhook URL option. This is a sample of the POST data sent to a alert webhook URL:
```
{
    "stocks": "SEPOWER,ASTEC,EDUCOMP,KSERASERA,IOLCP,GUJAPOLLO,EMCO",
    "trigger_prices": "3.75,541.8,2.1,0.2,329.6,166.8,1.25",
    "triggered_at": "2:34 pm",
    "scan_name": "Short term breakouts",
    "scan_url": "short-term-breakouts",
    "alert_name": "Alert for Short term breakouts",
    "webhook_url": "http://your-web-hook-url.com"
}
```
This PHP script receives and formats such data, and sends it to the Telegram user whose ID is passed in the get variable ```tgt```. A POST request is made to the Telegram API for this. Before using, you need to have a Telegram bot and replace XXXXXXXXXX in the script with your bot's token.

## Sample Telegram Alert:

![Picture](https://raw.githubusercontent.com/DinVyapari/chartink-bot/master/alert.jpg)

You need a Chartink Premium subscription for live scans.

## To Do:

- [ ] Add a database to store and process alerts.
- [ ] Implement algo trading.
- [ ] Check OI/Volume of scan results for confirmation.
