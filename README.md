---

# 🚀 Scalable Static Website with S3 + Cloudflare + GitHub Actions

## 📌 Project Overview



* **AWS S3** for storage & static hosting
* **Cloudflare** for DNS, CDN, caching, and free SSL
* **GitHub Actions** for CI/CD automation

Whenever I push code to GitHub, my website automatically updates on **S3** and Cloudflare cache is purged, ensuring instant updates across the globe.

---

## 🛠️ Tools & Technologies

* **AWS S3 (Free Tier)** – Website hosting
* **Cloudflare (Free)** – DNS, CDN, HTTPS, caching, performance
* **GitHub Actions** – CI/CD workflow automation
* **HTML & CSS** – Static website content
* **Bash & AWS CLI** – Bucket policy & configuration

---

## 🔑 Steps I Followed

### 1. Project Setup

* Created a GitHub repo with `index.html` and `style.css`.
* Registered a domain and connected it to Cloudflare.

### 2. S3 Hosting

* Created an **S3 bucket** (same name as domain).
* Enabled static website hosting.
* Applied a bucket policy to allow public access.

### 3. IAM & GitHub Secrets

* Created an IAM user with limited S3 access.
* Stored credentials in GitHub repo secrets:

  * `AWS_ACCESS_KEY_ID`
  * `AWS_SECRET_ACCESS_KEY`
  * `S3_BUCKET_NAME`
  * `CLOUDFLARE_API_TOKEN`
  * `CLOUDFLARE_ZONE_ID`

### 4. GitHub Actions Workflow

* Added `.github/workflows/deploy.yml with steps:

  1. Checkout code
  2. Configure AWS credentials
  3. Sync files to S3
  4. Purge Cloudflare cache

### 5. Cloudflare Setup

* Configured DNS (CNAME → S3 endpoint).
* Enabled **SSL/TLS Flexible mode**.
* Enabled **Auto Minify (HTML/CSS/JS)** and **Brotli compression**.
* Set caching rules for static assets.

### 6. Testing & Verification

* Edited `index.html`, committed & pushed.
* GitHub Actions ran and deployed files.
* Site updated instantly on `https://yourdomain.com`.

---

## ✅ Deliverables

* Live HTTPS site served via Cloudflare CDN.
* Automated deployment pipeline with GitHub Actions.
* Global caching + performance optimization.
* Screenshots included:

  * S3 hosting panel
  * Bucket policy
  * Cloudflare DNS settings
  * Cloudflare SSL/TLS settings
  * GitHub Actions run
  * Live site with HTTPS lock

---

## 📷 Sample Screenshots
<img width="1897" height="972" alt="Screenshot 2025-09-16 192908" src="https://github.com/user-attachments/assets/f3a63450-c6db-41d2-8941-34021b51c3d1" />
<img width="1918" height="970" alt="Screenshot 2025-09-16 192745" src="https://github.com/user-attachments/assets/58904c56-3082-4806-b44f-fbd068b6552c" />
<img width="1917" height="1017" alt="Screenshot 2025-09-16 192437" src="https://github.com/user-attachments/assets/bc6acf5e-cc18-4d26-a955-e6484dcd518e" />
<img width="1918" height="1015" alt="Screenshot 2025-09-16 193005" src="https://github.com/user-attachments/assets/6d33073f-0987-47cd-b622-4f4104b5cdbf" />
<img width="1913" height="1002" alt="Screenshot 2025-09-16 193412" src="https://github.com/user-attachments/assets/0d4b9550-cefd-405a-b1a5-9efe345ab8f9" />

---

## 📖 Conclusion

This project shows how to build a **scalable, cost-effective static website hosting solution** with AWS + Cloudflare + GitHub Actions. It eliminates manual deployments, provides global performance, and ensures secure HTTPS access with automated updates on every commit.

---

✨ Future improvements could include GitHub OIDC for secure deployments, cache-busting for assets, and adding staging environments.

---
