---
layout:            post
title:             "Send and Receive Emails Using Your Own Domains For Free"
date:              2016-06-14 17:00:00 -0700
tags:              Email Domain
category:          Readme
---

Bought you own domain? Do you want to send and receive emails with your own domain name? There are a couple of options out there, [G Suite](https://gsuite.google.com) for a minimun of $5/mo, or [zoho](https://www.zoho.com) will be cheaper for $1/mo, or maybe your domain provider will also provide support for email hosting, ranging from $2/mo to $5/mo. Excluding from serving your own eamil server, if you want a reliable email servie with your custom domain, there aren't a lot of choices there. Today, I will a way that you can send and receive emails with your own domain, and for totally free.

## Prerequisite

- A domain such as this super one [lowerCamelCase.com](https://www.lowercamelcase.com) and access to its DNS record.
- A email service that can support `Send Mail As`, [Gmail](https://mail.google.com) might be the most popular one, or you can choose your own preference as long as it supports adding another SMTP account.

## Now let's begin

The trick to send and receive emails for free is [mailgun](https://www.mailgun.com). So go to their website and signup for a new account. Your credit card won't be charged as long as the amount of your monthly emails stays in thier free cap. 

![]({{ "/assets/screenshots/2019-06-16-17.19.22.png#left" | absolute_url }})

Once signed up and logged into their dashboard, go to `Sending > Domains`. The dashboard should appear on the left side.

Now click `Add New Domain` and then input your domain name and select your region.

> If you want to send emails from your root domain, for example me@lowercamelcase.com, you should input lowercamelcase.com instead of mg.lowercamelcase.com though mailgun recommended so.

After adding your domain, follow the instructions shown on the page and go to your DNS provider to add those records. Then click `Verify DNS Settings`, if all the line items shows green, you're good to go.

Now back to the side bar and click `Receiving`, then click `Create Route`. In the `Expression Type`, select `Catch All`, enable this rule mailgun will forward all the emails send to `*@lowercamelcase.com`. In the forward section, simply add the email address you are going to receive.


