# Mango Ground Bakery Website

A simple static website showcasing the bakery’s products and services. This site is built with plain HTML and CSS, intended for easy deployment as a static web app.

---

## Cloud Provider Used

Microsoft Azure Static Web Apps — a service optimized for static front-end web apps with automated GitHub-based deployment.

---

## Deployment Steps

1. **Upload your site files to GitHub**  
   Uploaded `index.html` and other assets to a GitHub repository named `black-goose-bakery`.

2. **Create Azure Static Web App**  
   - Logged into [Azure Portal](https://portal.azure.com).  
   - Created a new Static Web App resource with the following settings:  
     - Subscription: Azure for Students  
     - Resource Group: `black-goose`  
     - App name: `black-goose-bakery`  
     - Region: Global (default)  
     - Deployment source: GitHub (linked to repository and branch `main`)  
     - Build presets: Custom  
     - App location: `/` (root directory)  
     - API location: *(left blank)*  
     - Output location: *(left blank)*

3. **GitHub Actions Workflow**  
   Azure created a workflow at `.github/workflows/azure-static-web-apps.yml` that automatically builds and deploys the app on pushes to `main`.

4. **Monitor Deployment**  
   Deployment progress was tracked on GitHub Actions and the Azure Static Web Apps resource page. Once complete, the site became publicly accessible.

---

## Problems Encountered & Solutions

- **Initial “Your site will be ready soon” message:**  
  This appeared because the deployment workflow was still running or hadn’t started yet.  
  *Solution:* Waited for GitHub Actions to complete the deployment or triggered a manual redeploy by pushing a new commit.

- **Workflow errors or missing workflow:**  
  Verified the GitHub repository and branch linkage, and confirmed the workflow YAML file existed in the `.github/workflows` directory.

- **App location setting:**  
  Ensured `App location` was set to `/` since `index.html` was in the root of the repository.

---

## Access Information

- **Public URL:**  
  [https://mango-ground-07fa02e10.6.azurestaticapps.net/](https://mango-ground-07fa02e10.6.azurestaticapps.net/)

Visit this URL to see the live bakery website.

---


