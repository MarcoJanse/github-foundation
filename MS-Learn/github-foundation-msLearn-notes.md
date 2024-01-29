# GitHub Foundation MS-Learn notes

## Index
- [GitHub Foundation MS-Learn notes](#github-foundation-ms-learn-notes)
  - [Index](#index)
  - [Introduction to Git](#introduction-to-git)
    - [Basic commands](#basic-commands)
    - [Fix mistakes](#fix-mistakes)
    - [Branching](#branching)
  - [Introduction to GitHub products](#introduction-to-github-products)
    - [GitHub accounts and plans](#github-accounts-and-plans)
      - [Account types](#account-types)
      - [GitHub plans](#github-plans)
  - [GitHub Codespaces](#github-codespaces)

## Introduction to Git

### Basic commands

```bash
# Set user name globally
git config --global user.name "<USER_NAME>"

# Set user email globally
git config --global user.email "<USER_EMAIL>"

# List config
git config --list

# Initialize repo
git init --initial-branch=main
## or
git init -b main

# view previous commits
git log
```

### Fix mistakes

```bash
# recover deleted file
git checkout -- <deleted_filename>

# recover deleted file removed with git rm
git reset HEAD <deleted_filename>
# then use checkout again to recover

# Revert previous commit
git revert --no-edit HEAD
```

### Branching

```bash
# Create branch
git checkout -b <branch-name>

# merge branch from main
git merge <branch-name> --no-edit
git push

# resolve merge conflict
## abort merge
git merge --abort 
    #or
got reset --hard
## or resolve manually in code editor
```

## Introduction to GitHub products

### GitHub accounts and plans

#### Account types

- **Personal**
  - Uses _Free_ or _Pro_ plan
- **Organization**
  - Can use RBAC for users within organizations
  - High privilege roles:
    - organization owners
    - security managers
- **Enterprise**
  - Enables inner sourcing
  - Centrally manage billing and policies
  - Must have a handle (organization or user account)

#### GitHub plans

- **GitHub free for personal accounts**
  - 500 MB package storage
  - 120 Codespaces hours/month
  - 15 GB Codespaces storage
  - 2000 minutes/month GitHub actions
- **GitHub free for organizations**
  - ++ Team access controls for managing groups
- **GitHub Pro for personal accounts**
  - GitHub support
  - 2 GB GitHub Packages storage
  - 3000 minutes/month GitHub actions
  - 180 Codespaces hours/month
  - 20 GB Codespaces storage
  - Advanced tools & insights
- **GitHub Team**
  - Same as GitHub Pro with added features
  - ++ Draft PR
  - ++ Team PR reviewers
  - ++ Scheduled reminders
- **Github Enterprise**
  - GitHub Enterprise Server
    - Self hosted
  - _GitHub Enterprise Cloud_
    - 50,000 GitHub Actions minutes per month
    - 50 GB GitHub Packages storage
    - A service level agreement for 99.9% monthly uptime
    - Option to centrally manage policy and billing for multiple GitHub.com organizations with an enterprise account
    - Option to provision and manage the user accounts for your developers, by using Enterprise Managed Users

## GitHub Codespaces

- Default timeout for codespace is 30 minutes
- Default retention for inactive codespace is 30 days
