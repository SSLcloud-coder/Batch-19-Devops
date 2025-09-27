# 📘 Git Notes

## 1. What is Git?

-   Git is a **Distributed Version Control System (DVCS)**.\
-   Created by **Linus Torvalds** in 2005 (the same person who created
    Linux).\
-   It helps **track changes in source code** during software
    development.\
-   It allows **multiple developers** to work together on the same
    project **without overwriting each other's work**.

👉 Think of Git as a **time machine for code**. You can go back to old
versions, compare changes, and collaborate easily.

------------------------------------------------------------------------

## 2. Why do we use Git? (Need & Reasons)

  -----------------------------------------------------------------------
  Problem (Without Git)                    Solution with Git
  ---------------------------------------- ------------------------------
  Multiple developers overriding each      Git merges code changes safely
  other's code                             

  No history of changes                    Git stores complete version
                                           history

  Hard to roll back to older code          Git allows easy rollback

  Sharing code via email/zip files         Git enables central repo
                                           (GitHub, GitLab, etc.)

  No proper teamwork tracking              Git has **branches, commits,
                                           tags**
  -----------------------------------------------------------------------

👉 **Main reasons:**\
- **Collaboration** (teamwork without conflicts)\
- **Version Control** (track who changed what and when)\
- **Backup** (remote repo keeps code safe)\
- **Rollback** (restore to previous working version anytime)\
- **CI/CD Integration** (works smoothly with DevOps pipelines)

------------------------------------------------------------------------

## 3. Role of Git in DevOps & Cloud

-   **DevOps** = Development + Operations → need automation &
    collaboration.\
-   Git is the **foundation of DevOps pipelines**.

### 🔹 Role in DevOps

1.  **Source Code Management (SCM)** → Store, manage, and version code.\
2.  **Collaboration** → Developers, testers, and ops team can work
    together.\
3.  **Automation** → Git integrates with Jenkins, GitLab CI, Azure
    DevOps, etc.\
4.  **Infrastructure as Code (IaC)** → Terraform, Ansible, Kubernetes
    YAML files are also stored in Git.\
5.  **Rollback & Audit** → Easy to track issues and fix quickly.

### 🔹 Role in Cloud

-   Cloud platforms (AWS, Azure, GCP) integrate Git for **code
    deployment**.\
-   Example: Push code → Trigger pipeline → Deploy on cloud servers.\
-   Git is used for:
    -   **Serverless apps** (Lambda, Azure Functions)\
    -   **Container deployments** (Docker + Kubernetes)\
    -   **Infrastructure automation**

👉 Without Git, DevOps automation is **not possible**.

------------------------------------------------------------------------

## 4. Alternatives to Git (Other Repositories)

There are other **Version Control Systems (VCS)** besides Git.

### 🔹 Older Centralized VCS

1.  **CVS (Concurrent Versions System)** -- very old, rarely used now.\
2.  **SVN (Apache Subversion)** -- centralized, still used in some
    companies.\
3.  **Perforce (Helix Core)** -- powerful, used in gaming & enterprise
    apps.\
4.  **Mercurial (Hg)** -- similar to Git but less popular now.\
5.  **Bazaar (BZR)** -- Canonical's system, used in Ubuntu development
    (now discontinued).

### 🔹 Git-based Platforms (Repositories to host Git projects)

These are **cloud-based Git repositories**:\
1. **GitHub** -- most popular, community + enterprise use.\
2. **GitLab** -- CI/CD built-in, used in DevOps.\
3. **Bitbucket** -- from Atlassian (supports Git & Mercurial).\
4. **Azure Repos** -- part of Azure DevOps (Microsoft).\
5. **AWS CodeCommit** -- Git repository hosted on AWS.\
6. **Google Cloud Source Repositories** -- Git repos on GCP.

👉 **Difference:**\
- Git = Version Control Tool\
- GitHub/GitLab/Bitbucket = Cloud platforms to host Git repositories

------------------------------------------------------------------------

## 5. Types of Git Repositories

  -----------------------------------------------------------------------
  Repo Type             Description              Example Use
  --------------------- ------------------------ ------------------------
  **Local Repo**        Stored on your own       Developer working
                        machine                  offline

  **Remote Repo**       Hosted on cloud server   Team collaboration
                        (GitHub, GitLab, etc.)   

  **Bare Repo**         Repo without working     Central repo for sharing
                        directory, only version  
                        history                  

  **Forked Repo**       Copy of someone else's   Open-source
                        repo, independent        contributions
                        development              

  **Mirror Repo**       Exact clone (read-only)  Large enterprises backup
                        for backup/mirror        
  -----------------------------------------------------------------------
