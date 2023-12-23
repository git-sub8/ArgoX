#【ArgoX】 = Argo + Xray

* * *

# Table of contents

- [Update information](README.md#Update information)
- [Project Features](README.md#Project Features)
- [ArgoX for VPS run script](README.md#argox-for-vps-run script)
- [Get Argo Json](README.md#argo-json-Get)
- [Getting Argo Token](README.md#argo-token-getting)
- [Disclaimer](README.md#Disclaimer)

* * *
## Update information
2023.4.13 1.0 official version

<details>
     <summary>History update history (click to expand or collapse)</summary>
<br>

>2023.3.11 beta6 1. Users can easily obtain the JSON of a fixed domain name tunnel through the accompanying function website at https://fscarmen.cloudflare.now.cc; 2. Change the sensitive path names; 3. Add CDN for download; 1. Users can easily obtain the json of the fixed domain name tunnel through the supporting function network, https://fscarmen.cloudflare.now.cc; 2. Change the sensitive path name; 3. Download and add CDN
>
>2023.3.4 beta5 1. Change listening to all network addresses to only Argo tunnel directed listening for added security; 2. Argo Tunnel supports dualstack; 1. Change listening to all network addresses to only Argo tunnel directed listening for added security; Increase security; 2. Argo tunnel supports dual stack
>
>2023.3.2 beta4 Change listening to all network addresses to only Argo tunnel directed listening for added security; Change listening to all network addresses to only Argo tunnel directed listening for added security;
>
>2023.2.24 beta3 1. Simplify the operation of changing argo tunnel; 2. Use wget global instead of cURL; 1. Simplify the method of converting Argo tunnel; 2. Use wget global instead of cURL
>
>2023.2.17 beta2 1. extremely fast installation mode, [-f] followed by a parameter file path; 2. Support for switching between the three argo tunnels; 3. Synchronise Argo and Xray to the latest version at any time; 4. Optimize the code to achieve speedup.
>1. Extremely fast installation mode, [-f] followed by parameter file path; 2. After installation, three argo tunnels are supported to switch at will; 3. Synchronize Argo and Xray to the latest version at any time; 4. Optimize the code to achieve speed improvement .
</details>

2023.2.16 beta1 Argo + Xray for vps


## Project Features:

* Deploy Xray in VPS, using the solution Argo + Xray + WebSocket + TLS;
* Normally CF is used to access the computer room and return to the source. Argo creates two reverse links to two nearby computer rooms each time, and then the return to the origin is through the source server to the nearest computer room. The user accesses the computer room and connects to the nearest computer room connected to the source server. In between is CF’s own black box line;
* Using CloudFlare's Argo tunnel, application traffic can be securely transmitted to the Cloudflare network using TLS encrypted communication, improving application security and reliability. In addition, Argo Tunnel can also prevent network threats such as IP leaks and DDoS attacks;
* Argo is a tunnel that penetrates the internal network. Xray's inbound does not expose the port to the outside world to increase security, and there is no need to waste resources by camouflaging the network. It also supports all ports of Cloudflare and will not stick to 443 and be blocked. At the same time, the server outputs Argo Ws Data flow greatly simplifies the data processing process and improves response. TLS is provided by cf to avoid multiple TLS;
* Argo tunnel supports both temporary tunnels and fixed domain names applied for through Token or cloudflared Cli. It is directly preferred + tunnel. There is no need to apply for a domain name certificate, and it can be converted at any time after installation;
* Fall back to offloading, and support Xray’s 4 mainstream protocols at the same time: vless / vmess / trojan / shadowsocks + WSS (ws + tls);
* The uuid of vmess and vless, the password of trojan and shadowsocks, and the ws path of each protocol can be customized or use the default value;
* Node information is output in V2rayN / Clash / Little Rocket link mode;
* Extremely fast installation, which can be installed interactively or non-interactively like docker compose. All parameters are put into a configuration file in advance, and the whole process takes less than 5 seconds.


## ArgoX for VPS run script:

```
bash <(wget -qO- https://raw.githubusercontent.com/fscarmen/argox/main/argox.sh)
```

```
wget https://raw.githubusercontent.com/zsdbbn/suoha-reality/main/suoha.sh -O suoha.sh && bash suoha.sh
```
   | Option parameters | Remark remarks |
   | -----------| ------ |
   | -c | Chinese 中文 |
   | -e | English English |
   | -f | Variable file, refer to REPO file "config" parameter file, file that can parameterize the project config |
   | -u | Uninstall uninstall |
   | -e | Export Node list displays node information |
   | -v | Sync Argo Xray to the newest Synchronize Argo Xray to the latest version |


## Argo Json acquisition

Users can easily obtain it through the Cloudflare Json generation network: https://fscarmen.cloudflare.now.cc

![image](https://user-images.githubusercontent.com/62703343/224388718-6adf22d0-01d3-46a0-8063-bc0a2210795f.png)

If you want to do it manually, you can refer to, taking Debian as an example, the commands you need to use, [Deron Cheng - CloudFlare Argo Tunnel trial](https://zhengweidong.com/try-cloudflare-argo-tunnel)


## Obtaining Argo Token

Detailed tutorial: [Synology Suite: Cloudflare Tunnel intranet penetration Chinese tutorial supports DSM6 and 7](https://imnks.com/5984.html)

<img width="1409" alt="image" src="https://user-images.githubusercontent.com/92626977/218253461-c079cddd-3f4c-4278-a109-95229f1eb299.png">

<img width="1619" alt="image" src="https://user-images.githubusercontent.com/92626977/218253838-aa73b63d-1e8a-430e-b601-0b88730d03b0.png">

<img width="1155" alt="image" src="https://user-images.githubusercontent.com/92626977/218253971-60f11bbf-9de9-4082-9e46-12cd2aad79a1.png">


## Disclaimer:
* This program is for learning and understanding only. It is for non-profit purposes. Please delete it within 24 hours after downloading. It may not be used for any commercial purposes. The text, data and pictures are copyrighted. If reproduced, the source must be indicated.
* Use of this program must comply with the deployment disclaimer. The use of this program must comply with the laws and regulations of the country where the server is deployed, the country where it is located, and the country where the user is located. The program author is not responsible for any inappropriate behavior by the user.
