
---

# 🚀 Deployment Instructions for React Portfolio Website

This document outlines the complete process for deploying your **React Portfolio Website** using **GitHub Pages** and a **custom domain (`kartikk.site`) from Hostinger**.

It also explains how to **update the site** in the future after making code changes.

---

## 🛠️ Step 1: Push Code to GitHub

1. Create a new repository on **GitHub**.

2. Initialize your React project locally:

   ```bash
   npx create-react-app my-portfolio
   ```

3. Push the code to the `main` branch:

   ```bash
   git add .
   git commit -m "Initial commit"
   git push origin main
   ```

---

## 🌿 Step 2: Configure Deployment with `gh-pages`

1. Install the `gh-pages` package:

   ```bash
   npm install gh-pages --save-dev
   ```

2. In your `package.json`, add the `homepage` field:

   ```json
   "homepage": "https://kartikk-26.github.io/<your-repo-name>"
   ```

3. Add the following scripts to the `scripts` section:

   ```json
   "scripts": {
     "predeploy": "npm run build",
     "deploy": "gh-pages -d build"
   }
   ```

4. Deploy the project:

   ```bash
   npm run deploy
   ```

   This will automatically create a `gh-pages` branch and publish the build files.

---

## ⚙️ Step 3: Enable GitHub Pages

1. Go to your **GitHub repository → Settings → Pages**.
2. Under **Source**, select:

   ```
   Branch: gh-pages
   ```
3. GitHub will publish your site at:

   ```
   https://kartikk-26.github.io/<your-repo-name>
   ```

---

## 🌐 Step 4: Set Up Custom Domain (Hostinger)

1. Purchase your domain via **Hostinger** (already done: `kartikk.site`).

2. In **Hostinger DNS Settings**, add the following records:

   * **A Records** (Pointing to GitHub Pages IPs):

     ```
     185.199.108.153
     185.199.109.153
     185.199.110.153
     185.199.111.153
     ```

   * **CNAME Record**:

     ```
     www → kartikk-26.github.io
     ```

3. Wait for **DNS propagation** (can take a few minutes to several hours).

---

## 🔗 Step 5: Connect Custom Domain in GitHub Pages

1. Go to **GitHub Repo → Settings → Pages**.

2. In the **Custom domain** field, enter your domain name:

   ```
   kartikk.site
   ```

3. Enable **Enforce HTTPS** for a secure connection.

✅ Your website is now live at:

```
https://kartikk.site
```

---

## 🔄 Step 6: Update Website After Changes

To reflect updates on the live website:

1. Commit your code changes:

   ```bash
   git add .
   git commit -m "Updated portfolio"
   git push origin main
   ```

2. Redeploy the project:

   ```bash
   npm run deploy
   ```

3. GitHub will rebuild and update the `gh-pages` branch.

No further DNS or domain setup is needed for future updates.

---

## 🧰 Summary of Tools Used

| Tool               | Purpose                          |
| ------------------ | -------------------------------- |
| **React.js**       | Frontend framework               |
| **GitHub**         | Version control & code hosting   |
| **GitHub Pages**   | Free static site hosting         |
| **gh-pages** (NPM) | Deployment automation            |
| **Hostinger**      | Domain provider (`kartikk.site`) |

---

## ✅ Final Deployment Overview

* **Repository**: [`https://github.com/kartikk-26/<your-repo-name>`](https://github.com/kartikk-26/<your-repo-name>)
* **Live Website**: [`https://kartikk.site`](https://kartikk.site)
* **Deployment Branch**: `gh-pages`

---


