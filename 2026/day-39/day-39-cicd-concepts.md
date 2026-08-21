# Day 39 – What is CI/CD?

##  What I Learned

Today I learned the basic concepts of CI/CD and how a CI/CD pipeline helps developers build, test, and deploy applications automatically.

---

# Task 1: The Problem

Imagine 5 developers working on the same project and manually deploying the application.

### What can go wrong?

* Due to manual deployment there are many errors in the code
* Its high chance to miss any step during manual deployment.
* Code may work on one computer but fail on another.
* Testing may be missed.
* Configuration can be varries in the environments.
* Manual deployment takes more time to market.
* A small mistake can cause deployment failure.

### What does "It works on my machine" mean?

It means the application works on the developer's computer but does not work on another computer or server.

This can happen because of different:

* Operating systems
* Software versions
* Dependencies
* Configurations
  
CI/CD helps by using an automated and consistent process.

### How many times can we safely deploy manually?

There is no fixed number.But the more frequently we deploy manually, the greater the chance of human mistakes.
CI/CD makes frequent deployments easier and safer by automating the process.

---

# Task 2: CI vs CD

## Continuous Integration (CI)

CI means developers frequently push their code to a shared repository.

Whenever code is pushed, the CI system automatically builds and tests the code.

### Simple Example

```text
Developer
    ↓
Push Code
    ↓
GitHub
    ↓
Build
    ↓
Run Tests
    ↓
Pass / Fail
```

### What CI catches

* Build errors
* Test failures
* Code integration problems
* Dependency problems

---

## Continuous Delivery

Continuous Delivery means that after the code passes testing, it is prepared and kept ready for deployment.

Production deployment may still require a manual approval.

### Example

```text
Push Code
   ↓
Build
   ↓
Test
   ↓
Docker Image
   ↓
Staging
   ↓
Manual Approval
   ↓
Production
```

---

## Continuous Deployment

Continuous Deployment means that code is automatically deployed to production after all required checks pass.

There is no manual approval for every release.

### Example

```text
Push Code
   ↓
Build
   ↓
Test
   ↓
Docker Image
   ↓
Production
```


# Task 3: Pipeline Anatomy

A CI/CD pipeline contains different parts.

## 1. Trigger

A trigger starts the pipeline.

Examples:

```text
git push
Pull Request
Manual trigger
Scheduled trigger
```

---

## 2. Stage

A stage is a major part of the pipeline.

Examples:

```text
Build
Test
Deploy
```

---

## 3. Job

A job is a group of tasks that run together.

Example:

```text
Test Stage
   ├── Unit Test
   └── Integration Test
```

---

## 4. Step

A step is one command or action inside a job.

Example:

```bash
npm install
npm test
docker build .
```

---

## 5. Runner

A **runner** is the machine that runs the pipeline.

For example:

```text
GitHub Actions
      ↓
Ubuntu Runner
      ↓
Runs commands
```

---

## 6. Artifact

An artifact is something produced by the pipeline.

Examples:

* JAR file
* ZIP file
* Test report
* Docker image

---

# Task 4: CI/CD Pipeline Diagram

### Scenario

A developer pushes code to GitHub. The application is:
1. Tested
2. Built into a Docker image
3. Deployed to a staging server


# Task 5: Explore in the Wild

## Repository

I explored the FastAPI open-source repository.

GitHub:
https://github.com/fastapi/fastapi.git

Workflow directory:

```text
.github/workflows/
```

I opened a build-docs.yml file to understand how GitHub Actions is used.

### What triggers it?

The workflow uses the `on:` section to define when it should run.

Example:

```yaml
on:
  push:
```

This means the workflow can automatically run when a code is pushed.

### How many jobs does it have?

The jobs are defined under:

```yaml
jobs:
```

Each entry under `jobs` represents a job. There are 4 jobs present in this. 

### What does it do?

It checks documentation and build documentation in various languages and completed the workflow.
---




