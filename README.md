# Static-Egress-IP-Gateway-for-API-IP-Allowlisting

Need a Fixed Outbound IP for Your API/IP Allowlisting? We provide a managed Static Egress IP Gateway via an HTTPS proxy.

## Why Choose Us?
- **Static Outbound IPv4** (Shared or Dedicated)
- **HTTPS CONNECT 80 443 only** (NOT a VPN. Other service ports DM communication)
- **Strict Domain Allowlist** (wildcards supported)
- **Blocks Private/Reserved IP Ranges** (SSRF protection)
- **Metered by Bytes** + **Hard Traffic Cap**
- **Auto-pause at Quota** (hard stop), top-up to resume instantly

## Perfect for:
- Apps on **Vercel**, **Netlify**, **Render**, **Cloud Run** needing IP allowlisting
- Integrations with **corporate firewalls**
- **APIs** and **Databases** requiring allowlisted source IPs

## 🌐 Common Platforms and Services Requiring Static IP for Allowlisting

### 🧩 Cloud Services & Hosting Platforms (Outbound requests need allowed IPs)
- **Vercel** – Default dynamic IP, requires Static IP or Secure Compute for allowlisting outbound requests. ([Vercel Docs](https://vercel.com/guides/how-to-allowlist-deployment-ip-address?utm_source=chatgpt.com))
- **Netlify Functions / Serverless** – Dynamic outbound IP, requires VPC or static proxy for API allowlisting.
- **Google Cloud Run** – Default dynamic IP, requires VPC and static NAT IP. ([Google Cloud Docs](https://docs.cloud.google.com/run/docs/configuring-static-outbound-ip?utm_source=chatgpt.com))
- **Google Cloud Functions / Firebase Functions** – Same as Cloud Run, static outbound IP requires VPC and Cloud NAT. ([StackOverflow](https://stackoverflow.com/questions/38811882/possible-to-get-static-ip-address-for-google-cloud-functions?utm_source=chatgpt.com))
- **AWS Lambda / API Gateway** – Dynamic outbound IP, requires NAT Gateway or managed NAT solution for allowlisting. ([StackOverflow](https://stackoverflow.com/questions/54598312/static-ip-for-outbound-api-calls?utm_source=chatgpt.com))
- **Heroku** – Dynamic outbound IP, can use add-ons or external static proxies for IP allowlisting.
- **Fly.io** – Dynamic outbound IP, users report difficulties with direct allowlisting. ([Fly.io Community](https://community.fly.io/t/set-get-outgoing-ip-address-for-whitelisting-on-external-apis-hosts/3690?utm_source=chatgpt.com))
- **Cloudflare Zero Trust Egress** – Allows obtaining Dedicated Egress IP for outbound allowlisting. ([Cloudflare Docs](https://developers.cloudflare.com/cloudflare-one/traffic-policies/egress-policies/dedicated-egress-ips/?utm_source=chatgpt.com))

### ☁️ PaaS / Hosted Apps & Serverless Architectures
- **Azure App Service / Azure Functions** – Static outbound IP requires configuration of service environment/ASE/VNet.
- **AWS Elastic Beanstalk / ECS / Fargate** – Requires VPC NAT for static outbound IP.
- **Google App Engine** – Requires additional network configuration for static IP.
- **Kubernetes Clusters (EKS/AKS/GKE)** – Requires NAT/Egress Controller for fixed outbound IP. ([Tigera.io Blog](https://www.tigera.io/blog/calico-egress-gateway-a-cost-effective-nat-for-kubernetes/?utm_source=chatgpt.com))

### 📡 SaaS / Integration / Enterprise Services Requiring IP Allowlisting
- **Enterprise APIs** (Stripe, PayPal, Bank APIs, etc.) – Typically require the caller's outbound IP to be whitelisted.
- **Database Services**  
  - MongoDB Atlas (requires source IP whitelisting)
  - AWS RDS (if public access or cross-VPC firewall)
  - Microsoft SQL Azure / PostgreSQL Hosted Services
- **CRM / ERP / Enterprise SaaS**  
  - Salesforce customer networks often require IP whitelisting
  - SAP / Oracle cloud configurations
- **Webhook Systems** (webhooks with strict security policies)
- **Corporate Firewalls** – Internal APIs or systems restricting external access to whitelisted IPs.

### 🚫 Other Common Use Cases Requiring IP Allowlisting
- Corporate firewalls/security domain policies
- Self-hosted API/Partner Private APIs
- Private cloud/data center systems that only allow specific external IPs
- Preventing security risks (SSRF protection)

---

### 📌 How These Scenarios Work

Many platforms do not provide **static outbound IPs** by default due to modern serverless/edge architectures that rely on dynamic IP pools. However, when you need to:

✔️ Communicate with **third-party APIs**  
✔️ The target system only allows IPs from whitelisted sources  
✔️ Your organization's security policies require access from specific IPs

You’ll need a **static outbound IP** (or a set of them) to be whitelisted for seamless communication.

---

## Plans & Pricing

### **BASIC — Trial (1GB)** ------ $1
- 1 shared static egress IPv4
- 1GB transfer (one-time)
- HTTPS CONNECT 80 443 only (NOT a VPN)
- Domain allowlist (up to 10 domains / wildcards)
- 24h–48h access (you decide)
- Setup instructions + test command
- Delivery: 8–12h
- The $1 trial fee can be credited toward your monthly subscription.

### **STANDARD — Shared IP (Monthly)** ------ $39
- 1 shared static egress IPv4
- 200GB/month (UTC cycle reset)
- Larger allowlist (up to 20 domains/wildcards)
- HA add-on：+2nd IP for failover (+$29)
- Logs: 7 days + usage snapshot on request
- Hard cap: auto-pause at quota, top-up to resume($10 / 100GB (=$0.10/GB))
- Delivery: 8–12h

### **PREMIUM — Dedicated IP (Monthly)** ------ $89
- 1 dedicated static egress IPv4 (exclusive)
- 800GB/month (UTC cycle reset)
- Larger allowlist (50+ domains/wildcards)
- HA add-on：+2nd IP for failover (+$49)
- Logs: 30 days + priority troubleshooting
- Hard cap + top-up($8 / 100GB (=$0.08/GB))
- Delivery: 8–12h

## Contact & Support
For inquiries or support, feel free to reach out via:
- **Email**: [Secserver03@proton.me]
- **Telegram**: [https://t.me/static2ip]

##To get started, send:
1) Region: SG / JP / US / EU /Other-DM
2) Allowed domains list (e.g., *.stripe.com, *.mongodb.net, partner.example.com)
3) Estimated monthly transfer (rough is fine)
