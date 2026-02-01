# CI Lab Project – Jenkins Continuous Integration

## Project Overview
This repository contains the implementation of a Continuous Integration (CI) pipeline using Jenkins as part of a DevOps laboratory assignment. The project demonstrates Jenkins installation, job configuration, and pipeline automation using both Freestyle and Multibranch Pipeline jobs.

---

## Tools & Technologies Used
- Jenkins (LTS)
- Java JDK 11+
- Git & GitHub
- Maven / Gradle
- Docker
- Windows OS
- Jenkins Plugins (Pipeline, Git, SCM, Testing, Notifications)

---

## Repository Structure
CILabProject/
├── src/
│ ├── main/
│ │ ├── java/com/muj/ci/
│ │ └── resources/
│ └── test/java/com/muj/ci/
├── docker/
│ └── Dockerfile
├── scripts/
│ ├── build.sh / build.bat
│ └── deploy.sh
├── Jenkinsfile
└── README.md

## Jenkins Jobs Implemented

### Job 1: Freestyle Project
- Connected to GitHub repository
- Build triggered using Poll SCM and Webhook
- Executes shell/batch commands
- Runs build and test scripts
- Post-build actions include archiving artifacts and test results

### Job 2: Multibranch Pipeline
- Automatically discovers branches from GitHub
- Uses Jenkinsfile for pipeline definition
- Different logic for:
  - main branch
  - feature branches
  - release branches
- Displays branch-wise build status and console output

## Jenkinsfile
The Jenkinsfile defines a declarative pipeline that includes:
- Source code checkout
- Build stage
- Test stage
- Branch-based execution logic

## How to Use This Project
1. Clone the repository
2. Open Jenkins dashboard
3. Configure Freestyle and Multibranch Pipeline jobs
4. Run builds and check console output

## Assignment Deliverables Covered
- Jenkins installation and configuration
- Jenkins architecture
- Freestyle and Multibranch jobs
- Jenkinsfile
- Console outputs and screenshots
- Documentation and reports

## Author
Tanima Mishra  
DevOps – CI Lab Assignment
