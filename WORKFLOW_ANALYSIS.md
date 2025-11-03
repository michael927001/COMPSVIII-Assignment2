# Workflow Analysis

**1. What triggers this workflow to run?**  
The workflow runs whenever code is pushed to the **main** branch. The `on: push: branches: [ "main" ]` section defines this trigger.

This workflow helped me understand real collaboration steps, especially how pull requests organize code changes for review.

**2. What are the four main steps this workflow performs?**
- Checkout the repository code
- Set up the GitHub Pages environment
- Build and deploy the website files
- Upload and publish the site to GitHub Pages

**3. What does the "Checkout code" step do and why is it necessary?**  
It downloads the repository files into the workflow runner so the deployment process has access to the website's code. Without it, GitHub Actions wouldn’t have files to deploy.

**4. What is the purpose of the environment configuration?**  
It ensures GitHub Pages is set as the deployment environment and manages permissions so only trusted workflows can publish site updates.

**5. How does this automated deployment improve reliability compared to manual deployment?**  
Automation prevents human error, ensures consistent deployment every time, and updates happen automatically when changes are pushed.

**6. What would happen if you pushed code to a different branch (not main)?**  
The workflow would **not run**, and the website would **not update**, because only pushes to `main` trigger deployment.
