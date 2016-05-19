---

title: Docs.microsoft.com contributor guide - Create/update an article in your local repo
description:
keywords:
author: bryanla
manager: 
ms.date: 05/19/2016
ms.topic: article
ms.prod:
ms.service: 
ms.technology:
ms.assetid: A269F1A3-CE8A-4F3F-A8FF-3FB44E276BB9

---

# Git commands for creating/modifying content using your local repository

Follow the steps below to create a local working branch on your computer, which you can use to update or create a new article for docs.microsoft.com.

1. Start Git Bash (or the command line tool you use for Git).

 **Note:** If you are working in a private repository, add the "-pr" suffix to all commands using a repository name.

2. Switch context to your `<repository-name>`. Recall that this maps to a local working directory on your computer, under the path `c:\users\user-account\repository-name\` :

        cd <repository-name>:
3. Set the current working branch to the 'master' branch:

        git checkout master

4. Pull down the latest changes for the 'master' branch in the docs.microsoft.com repository, and create a fresh local working branch derived from the master branch:

        git pull upstream master:<working-branch>


5. Set the current working branch to the branch just created

        git checkout <working-branch>

6. Push a copy of your working branch up to your fork:

        git push origin <working-branch>

7. Create your new article or make changes to an existing article, by creating/modifying files in the local working directory (`c:\users\user-account\repository-name\`). Use Windows Explorer to open and create new markdown files, and use your markdown editor to edit them.

8. As you create/modify/delete files in your working directory, you will want to "add" them to the staging area (aka: Index), then "commit" them from your working branch into your persisted copy of your branch, on a regular basis :

        git add -A
        git commit –m "<comment>"
        
   Or, to add only the specific files you modified:

        git add <file path>
        git commit –m "<comment>"

9. Update your local working branch with changes from upstream on a regular basis (recall `upstream` points to the docs.microsoft.com repository), so you pick up all of the latest changes since your last `pull` :

        git pull upstream master

10. Push the changes to your fork on GitHub (recall `origin` points to your forked repository, a copy of the docs.microsoft.com repository):

        git push origin <working-branch>

12. When you are ready to submit your content to the `upstream` master branch for staging, validation, and/or publishing, go back to the GitHub UI for your fork, and create a Pull Request from your fork's working branch, to the docs.microsoft.com repository's master branch. Click the "New pull request" button, with your fork/branch on the right (from), and the docs.microsoft.com repo/branch on the left (to). The page will also show you a comparison of the branches, so you can validate that the Pull Request contains the changes you think it should contain.

13. If you are an employee working in the private repository, a build report is sent to you via e-mail, and the changes you submit are automatically staged if the build completes successfully. Please review your staged content and indicate in the pull request comments whether you are signing off and ready for review/merge by the pull request reviewer.  This indicates the changes are ready to be pushed live. 

14. The pull request reviewer reviews your pull request, provides feedback, and/or merges your pull request. 

15. Optionally verify your published article or changes at the appropriate `http://docs.microsoft.com/*path to-your-article-without-the-MD-extension*` URL.

## Publishing

Articles are published at approximately 10:00 AM and 3:30 PM Pacific Time, Monday-Friday. It can take up to 45 minutes for articles to appear online after publishing. Remember your pull request has to be merged by a pull request reviewer before the changes can be included in the next scheduled publishing run. You need to work with your pull request reviewer ahead of time to ensure a pull request is merged for a specific publishing run. Otherwise, PRs are reviewed in the order they were submitted.

If you are an employee working in the private repository, all pull requests are subject to validation rules that need to be addressed before the pull request can be merged. 

## Working with release branches (Microsoft employees)

If you need to work with a release branch that has been created by the release manager, the best way to create a local working branch from the release branch is to use this command syntax:

    git checkout upstream/<release-branch-name> -b <local-working-branch-name>

This creates the local branch directly from the upstream branch, avoiding any local merging. The instructions for creating/updating/deleting content, pushing back to your fork, opening a Pull Request, etc., are the same as the instructions above for 'master' branch contributions, just use the release branch naming convention instead. When the release is ready, the release manager will merge the release branch into 'master'.

## Next steps

- If creating a new article, start with a copy of [the docs.microsoft.com markdown template](../template.md) 
- Back to the one-time [Install and setup tools for authoring GitHub content locally](./ContributorGuide/tools-and-setup.md)
- Back to [Step-by-step instructions](../readme.md#step-by-step) in main Contributor Guide

