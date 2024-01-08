# Mock Server Development Workflow

- [Mock Server Development Workflow](#mock-server-development-workflow)
  - [1. Add Mock Server as Git SubModule Dependency in Client Application.](#1-add-mock-server-as-git-submodule-dependency-in-client-application)
  - [2. Add new API's in MockServer Repository.](#2-add-new-apis-in-mockserver-repository)
  - [3. Update MockServer SubModule Dependency in Client Application.](#3-update-mockserver-submodule-dependency-in-client-application)


## 1. Add Mock Server as Git SubModule Dependency in Client Application.

```
git submodule add git@github.com:freshdesk/mobile_freshservice_mock_server.git
```

- This the one time process to add Mock Server as Git SubModule dependency in client application.

## 2. Add new API's in MockServer Repository.

- Before start developing new Data / Domain tasks in client application, we need to add new API's in MockServer repository.
- Create new branch in MockServer repository and Add new API (Route) in MockServer and stub all possible responses.
- Raise PR against `main`, get it reviewed and merge the PR.

## 3. Update MockServer SubModule Dependency in Client Application.

```
# Navigate to client app repo
cd [CLIENT_APP_PATH]

# Navigate to MockServer SubModule Repo
cd mobile_freshservice_mock_server

# Checkout the merged PR commit from main branch.
git checkout [COMMIT_HASH_MERGED_PR_FROM_MAIN_BRANCH]

# Navigate back to client app repo
cd ..


## Stage the changes
git add .

## Push the changes to client app repo
git commit -m "Updated MockServer SubModule to latest commit"
```