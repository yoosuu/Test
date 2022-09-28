---
title: "Init Genesis Block"
date : 2022-09-20T17:44:42+09:00
weight: 20
pre: "<b>B. </b>"
draft: false
---

{{< line_break >}}
### 4. Copy genesis.json under DATA directory

> *example : /var/kcnd/data/genesis.json*

{{< line_break >}}

### 5. Init Genesis block
##### 1) CN configuration
{{< highlight html >}}
$ kcn --networkid 7207 init --datadir /var/kcnd/data genesis.json
{{< /highlight >}}


##### 2) PN configuration
{{< highlight html >}}
$ kpn --networkid 7207 init --datadir /var/klaytn/kpnd/data genesis.json
{{< /highlight >}}

{{< line_break >}}

### 6. (ONLY PN) Create static-nodes.json and copy it under DATA directory
> *example : /var/kcnd/data/nodekey*

```vim
** Generate static-nodes.json **
You have 1 CN and 2 PNs, each are cn1, pn1, pn2.
1. static-nodes.json in pn1
   [
   "CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn",
   "PN2_KNI_ADDRESS@PN2_INTERNAL_IP:PORT?discport=0&ntype=pn"
   ]
2. static-nodes.json in pn2
   [
   "CN_KNI_ADDRESS@CN_INTERNAL_IP:PORT?discport=0&ntype=cn",
   "PN1_KNI_ADDRESS@PN1_INTERNAL_IP:PORT?discport=0&ntype=pn"
   ]
```

{{< line_break >}}
{{< line_break >}}


---
{{< line_break >}}
*You can check the more information for installation on the page below..*
* CN : https://docs.klaytn.foundation/node/core-cell/installation-guide/consensus-node-setup/configuration
* PN : https://docs.klaytn.foundation/node/core-cell/installation-guide/proxy-node-setup/configuration

{{< line_break >}}
{{< line_break >}}
{{< line_break >}}
If you finish this step, please click the next button ```>``` on the right side of this page.