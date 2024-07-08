## CI/CD Pipelines
**Tool:** Azure DevOps  
**Pipeline Configuration:** Azure Pipelines

---

### Front End Pipelines

1. **Commit and Push:**
   - Commit and push the latest code to the Azure repository.

2. **Create Pull Request:**
   - Create a pull request to the `main` branch.
   - CI trigger runs automatically.

3. **CI Stage - Build:**
   - Install Node.js.
   - Install project dependencies.
   - Run linting.
   - Run Gitleaks for secrets detection.
   - Run tests.
   - Run security audit.
   - Build the project.

4. **Merge to Main:**
   - Merge the pull request to the `main` branch.
   - CD trigger runs automatically.

5. **CD Stage - Deploy:**
   - Publish the latest source code to Vercel.

6. **Vercel Deployment:**
   - Vercel listens for changes and automatically deploys to the `main` branch.

![CI/CD Pipeline for Front End](/.attachments/CICD_FE-fc655631-990b-4f76-ade1-44717c319e49.png)

---

### Backend Pipelines

1. **Commit and Push:**
   - Commit and push the latest code to the Azure repository.

2. **Create Pull Request:**
   - Create a pull request to the `main` branch.
   - CI trigger runs automatically.

3. **CI Stage - Build:**
   - Install Node.js.
   - Install project dependencies.
   - Run linting.
   - Run Gitleaks for secrets detection.
   - Run tests.
   - Publish test results.
   - Run security audit.
   - Build the project.

4. **Merge to Main:**
   - Merge the pull request to the `main` branch.
   - CD trigger runs automatically.

5. **CD Stage - Build and Push Image:**
   - Build Docker image.
   - Push the image to Azure Container Registry.

6. **Azure Web App Deployment:**
   - Azure Web App triggers image pull from Azure Container Registry.
   - Automatically deploys to the `main` branch.

![CI/CD Pipeline for Backend](/.attachments/CICD_BE-5a500f1a-7054-46fa-a1e2-ead3f995f540.png)
