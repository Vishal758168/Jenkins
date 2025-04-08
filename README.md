# Jenkins Shared Library

This repository contains reusable pipeline code for Jenkins, structured as a shared library. It helps maintain clean, DRY, and modular Jenkinsfiles across multiple projects.

## 🛠 Usage

To utilize this shared library in your Jenkins pipeline:

1. **Configure the Shared Library in Jenkins:**
   - Navigate to **Manage Jenkins** → **Configure System** → **Global Pipeline Libraries**.
   - Add a new library with the following details:
     - **Name:** `jenkins-shared-library`
     - **Default Version:** Specify the branch to use, e.g., `main`.
     - **Retrieval Method:** Modern SCM.
     - **Source Code Management:** Git.
     - **Project Repository:** `https://github.com/elite-SR/Jenkins-shared-libraries.git`.

2. **Reference the Library in Your Jenkinsfile:**
   ```groovy
   @Library('jenkins-shared-library') _
   myCustomStep()
