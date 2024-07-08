
## CI/CD Pipelines
**Tool:** Azure DevOps  
**Pipeline Configuration:** Azure Pipelines

---

## Front End Pipelines

![CI/CD Pipeline for Front End](/.attachments/CICD_FE-fc655631-990b-4f76-ade1-44717c319e49.png)

1. **Commit and Push:**
   - Developers write code locally and commit their changes to the local Git repository.
   - These changes are then pushed to the remote Azure repository, initiating the CI process.

2. **Create Pull Request:**
   - A pull request (PR) is created to merge the new changes into the `main` branch.
   - This PR must be reviewed and approved by other team members.
   - Once the PR is created, the CI pipeline is triggered to validate the changes.

3. **CI Stage - Build:**
   - **Install Node.js:** The pipeline installs the required version of Node.js.
   - **Install Dependencies:** It runs `npm install` to install all necessary project dependencies.
   - **Run Linting:** The pipeline runs a linting tool (ESLint) to check the code for stylistic and programming errors.
   - **Run Gitleaks:** Gitleaks is executed to detect any hardcoded secrets and sensitive information in the codebase.
   - **Run Tests:** Automated tests are run to ensure that new changes do not break existing functionality.
   - **Run Security Audit:** The pipeline runs a security audit `npm audit --audit-level=high` to check for vulnerabilities in dependencies.
   - **Build the Project:** The project is built, typically using a command like `npm run build`.
4. **Merge to Main:**
   - After the PR is approved and merged into the `main` branch, the CD pipeline is triggered.

5. **CD Stage - Deploy:**
   - The pipeline publishes the latest source code to Vercel, a platform for front-end deployments.

6. **Vercel Deployment:**
   - Vercel listens for changes in the `main` branch and automatically deploys the updated application to the live environment.

---

### Backend Pipelines

![CI/CD Pipeline for Backend](/.attachments/CICD_BE-5a500f1a-7054-46fa-a1e2-ead3f995f540.png)

1. **Commit and Push:**
   - Developers write code locally and commit their changes to the local Git repository.
   - These changes are then pushed to the remote Azure repository, initiating the CI process.

2. **Create Pull Request:**
   - A pull request (PR) is created to merge the new changes into the `main` branch.
   - This PR must be reviewed and approved by other team members.
   - Once the PR is created, the CI pipeline is triggered to validate the changes.

3. **CI Stage - Build:**
   - **Install Node.js:** The pipeline installs the required version of Node.js.
   - **Install Dependencies:** It runs `npm install`, `npm install -g @nestjs/cli` and `npm run prisma:generate` to install all necessary project dependencies.
   - **Run Linting:** The pipeline runs a linting tool (ESLint) to check the code for stylistic and programming errors.
   - **Run Gitleaks:** Gitleaks is executed to detect any hardcoded secrets and sensitive information in the codebase.
   - **Run Tests:** Automated tests are run to ensure that new changes do not break existing functionality.
   - **Publish Test Results:** Test results are published to Azure DevOps for review.
   - **Run Security Audit:** The pipeline runs a security audit `npm audit --audit-level=high` to check for vulnerabilities in dependencies.
   - **Build the Project:** The project is built, typically using a command like `npm run build`.
4. **Merge to Main:**
   - After the PR is approved and merged into the `main` branch, the CD pipeline is triggered.

5. **CD Stage - Build and Push Image:**
   - **Build Docker Image:** The pipeline builds a Docker image of the application.
   - **Push to Azure Container Registry:** The Docker image is pushed to Azure Container Registry for storage and deployment.

6. **Azure Web App Deployment:**
   - Azure Web App triggers an image pull from Azure Container Registry.
   - The updated Docker image is automatically deployed to the live environment.