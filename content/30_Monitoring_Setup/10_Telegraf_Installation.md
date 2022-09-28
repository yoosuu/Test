---
title: "Telegraf Installation"
date: 2022-07-11T15:42:53+09:00
weight: 10
pre: "<b>A. </b>"
draft: false
---

{{< line_break >}}
### 1. Telegraf Installation
>Telegraf Installation Guide (Amazon Linux 2 users, see below):
{{< line_break >}}
https://docs.influxdata.com/telegraf/latest/introduction/installation/
{{< line_break >}}
> {{< line_break >}}
**Note for Amazon Linux 2**
{{< line_break >}}
To install Telegraph on Amazon Linux 2, you may use InfluxData's RHEL 7 yum repo as follows:


```vim
cat <<EOF | sudo tee /etc/yum.repos.d/influxdb.repo

[influxdb]
name = InfluxDB Repository - RHEL 7
baseurl = https://repos.influxdata.com/rhel/7/\$basearch/stable
enabled = 1
gpgcheck = 1
gpgkey = https://repos.influxdata.com/influxdb.key
EOF
```


{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.



