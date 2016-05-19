---

title: Docs.microsoft.com contributor guide - Tools and Setup
description:
keywords:
author: bryanla
manager: 
ms.date: 05/19/2016
ms.topic: article
ms.prod:
ms.service: 
ms.technology:
ms.assetid: 107118BE-02F4-4F91-BBC7-FD9BA630A60E

---

#Install and set up tools for authoring GitHub content locally

Follow the steps in this article to set up local tools for contributing to the docs.microsoft.com technical documentation stored on GitHub. 

If you're unfamiliar with Git, you might want to review some Git terminology: [https://help.github.com/articles/github-glossary](https://help.github.com/articles/github-glossary). In addition, this StackOverflow thread contains a glossary of Git terms you'll encounter in this set of steps: [http://stackoverflow.com/questions/7076164/terminology-used-by-git](http://stackoverflow.com/questions/7076164/terminology-used-by-git)

## Contents

- [Create a GitHub account and set up your profile](#create-a-github-account-and-set-up-your-profile)
- [Sign up for Lifefyre](#sign-up-for-lifefyre)
- [Determine whether you need to follow the rest of these steps](#determine-whether-you-really-need-to-follow-the-rest-of-these-steps)
- [Permissions in GitHub](#permissions-in-github)
- [Install Git for Windows](#install-git-for-windows)
- [Enable two-factor authentication](#enable-two-factor-authentication)
- [Install a markdown editor](#install-a-markdown-editor)
- [Fork the repository and copy it to your computer](#fork-the-repository-and-copy-it-to-your-computer)
- [Configure your user name and email locally](#configure-your-user-name-and-email-locally)
- [Next steps](#next-steps)

## Create a GitHub account and set up your profile

To contribute to the docs.microsoft.com technical content, you'll need a [GitHub](http://www.github.com) account.

**Note:** If you are a Microsoft employee, you need to set up your GitHub account so you're clearly identified as a Microsoft employee. Set up your profile as follows:

- **Profile picture**: a picture of you (required)
- **Name**: your first and last name (required)
- **Email**: your Microsoft email address (optional)
- **Company**: "Microsoft Corporation" (required)
- **Location**: list your location (optional)

Your profile should resemble this profile:

<p align="center">
 ![GitHub profile example](./media/tools-and-setup/githubprofile.png)

## Sign up for Lifefyre

Every published technical article supports a comment stream provided by the [Livefyre][Livefyre] service. If you wish to contribute comments (either general or "sidenote"), please see [How do I create a Livefyre Account](https://livefyre.zendesk.com/hc/en-us/articles/200329426-How-do-I-create-a-Livefyre-Account-) for details on sign up options. 

**Note:** If you are a Microsoft employee and article author or contributor, you need to sign up for Livefyre so you can participate in the comment stream for the article. Please use option *"b"* during sign up, *"Creating a Livefyre Account with a username, email, and password"*, so you can be easily identified when you post responses, and complete your profile as follows:

 - **Username**: your Microsoft email alias plus @MSFT, ie: *alias@MSFT*
 - **Email**: Your Microsoft.com email address.

## Determine whether you really need to follow the rest of these steps

If you did not land on this page from the [main page of the Contributor Guide](../readme.md), you may not need to follow all the steps in this article. As mentioned on the main Contributor Guide page, it depends on the magnitude of your contribution.

### Submitting minor contributions to an existing article

If you only need or want to make textual updates/corrections to an existing article, you probably don't need to follow the rest of the steps. You can use GitHub's Web-based markdown editor to submit your changes. Refer to the [Minor contributions: using the GitHub editor][UsingGithubEditor] section in the main Contributor Guide page.

### All other changes
When you work in the GitHub UI, you are limited in terms of what you can do. Managing branches can be confusing, for instance. So we typically recommend you install the tools and learn the commands for creating and managing articles in a local repository. 

For the following types of tasks, we strongly recommend you install and learn to use the tools for local authoring:

 - Making major changes to an article
 - Creating and publishing a new article
 - Adding new images or updating images
 - Updating an article over a period of days without publishing changes each of those days
 - Creating content for a release that has to go out on a certain day at a certain time

##Permissions in GitHub

Anybody with a GitHub account can contribute to docs.microsoft.com content through one of our [public repositories][DocsPubRepos]. No special permissions are required, as you have read access to public repositories by default.

**Note:** If you are a Microsoft employee, you must work in one of our private content repositories. First visit [https://opensourcehub.microsoft.com/](https://opensourcehub.microsoft.com/) to join your Github and Microsoft credentials for the GitHub "Microsoft" organization. Then ask a member of your content development team to add you to the appropriate GitHub team for read permissions in your private repository. Once you have read permissions, you will be able to fork the private repository later.

## Install Git for Windows

Install Software Freedom Conservancy's Git for Windows implementation from [http://git-scm.com/download/win](http://git-scm.com/download/win). This download installs the Git version control system, including Git Bash, the command-line app that you will use to interact with your local Git repository.

You can accept all default settings, unless you want different behavior (ie: commands Git commands are available within the Windows command line, for instance):

<p align="center">
 ![GitHub profile example](./media/tools-and-setup/gitbashinstall-282-1.png)
<p align="center">
 ![GitHub profile example](./media/tools-and-setup/gitbashinstall-282-2.png)
<p align="center">
 ![GitHub profile example](./media/tools-and-setup/gitbashinstall-282-3.png)
<p align="center">
 ![GitHub profile example](./media/tools-and-setup/gitbashinstall-282-4.png)
<p align="center">
 ![GitHub profile example](./media/tools-and-setup/gitbashinstall-282-5.png)

(Note: If you prefer a Graphical User Interface over a Command Line Interface, see [Software Freedom Conservancy's available GUI Clients page](https://git-scm.com/downloads/guis), [GitHub's GitHub Desktop](https://desktop.github.com/), or [Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx) for some popular options. Please note, however, that this guide is written from the point of view of a CLI user.

## Enable two-factor authentication

You have to enable two factor authentication (2FA) on your GitHub account if you are working in the private content repository. It's required in the private repository.

To enable this, follow the instructions in both the following GitHub help topics:

- [About Two-Factor Authentication](https://help.github.com/articles/about-two-factor-authentication/)
- [Creating an access token for command-line use](https://help.github.com/articles/creating-an-access-token-for-command-line-use/)

When you create the token, select all the scopes available in the token-creation UI ([details on each scope](https://developer.github.com/v3/oauth/#scopes))

After you enable 2FA, you have to enter the access token instead of your GitHub password at the command prompt when you try to access a GitHub repository from the command line. The access token is not the authentication code that you get in a text message when you set up 2FA. It's a long string that looks something like this:  fdd3b7d3d4f0d2bb2cd3d58dba54bd6bafcd8dee. A few notes about this:

- When you create your access token, save it in a text file to make it readily accessible when you need it.

- Later, when you need to paste the token, know there are two ways to paste in the command line:

 - Click the icon in the upper left corner of the command line window>Edit>Paste.
 - Right-click the icon in the upper left corner of the window and click Properties>Options>QuickEdit Mode. This configures the command line so you can paste by right-clicking in the command line window.

## Install a markdown editor

We author content using simple "markdown" notation in the files, rather than complex "markup" (HTML, XML, etc.). So, you'll need to install a markdown editor.

- **Atom**: GitHub's Atom Markdown editor: [http://atom.io](http://atom.io). It does not require a license for business use, and has spell check. After installation, you'll also need to set a few things up:
  - Atom defaults to using 2 spaces for tabs, but Markdown expects 4 spaces. If you leave it at the default of two, your article will look great in local preview, but not when it’s imported into Azure. So, configure Atom to use 4 spaces - you can find this setting under File>Settings>Editor Settings>Tab Length. 
  - You will probably also want to turn on Soft Wrap in this section too, which does the same as "word wrap" in Notepad. 
  - To turn on the markdown preview, click Packages>Markdown Preview>Toggle Preview. You can use Ctrl-Shift-M to toggle the preview HTML view.
- **Prose**: This is a lightweight, elegant, on-line, and open source Markdown editor that offers a preview. Visit [http://prose.io](http://prose.io) and authorize Prose in your repository.
- **[Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)** - A lightweight but powerful source code editor which runs on your desktop and is available for Windows, OS X and Linux. 
- **Notepad**: You can use Notepad for a very lightweight option.

## Fork the repository and copy it to your computer

1. Create a fork of the repository in GitHub - go to the top-right of the page and click the Fork button. If prompted, select your account as the location where the fork should be created. This creates a copy of the repository within your Git Hub account. Generally speaking, technical writers and program managers need to fork azure-content-pr, the private repo. Community contributors need to fork azure-content, the public repo. You only need to fork one time; after your first setup, if you want to copy your fork to another computer, you only have to run the commands that follow in this section to copy the repo to your computer.  If you choose to create forks of both repositories, you will need to create a fork for each repository.

2. Copy the Personal Access Token that you got from [https://github.com/settings/applications#personal-access-tokens](https://github.com/settings/applications#personal-access-tokens). You can accept the default permissions for the token.  Save the Personal Access Token in a text file for later reuse.

3. Next, copy the repository to your computer with your credentials embedded in the command string.  To do this, open Git Bash and run it as an administrator. At the command prompt, enter the following command.  This command creates a azure-content(-pr) drectory on your computer.  If you're using the default location, it will be at c:\users<your Windows user name>\azure-content(-pr).

Public repo:

        git clone https://[your GitHub user name]:[token]@github.com/<your GitHub user name>/azure-content.git

Private repo:

        git clone https://[your GitHub user name]:[token]@github.com/<your GitHub user name>/azure-content-pr.git

For example, this clone command could look something like this:

        git clone https://smithj:b428654321d613773d423ef2f173ddf4a312345@github.com/smithj/azure-content-pr.git  

## Set remote repository connection and configure credentials

Create a reference to the root repository by entering these commands. This sets up connections to the repository in GitHub so that you can get the latest changes onto your local machine and push your changes back to GitHub. This command also configures your token locally so that you don't have to enter your name and password each time you try to access the upstream repo and your fork on GitHub.

Public repo:

        cd azure-content
        git remote add upstream https://[your GitHub user name]:[token]@github.com/Azure/azure-content.git
        git fetch upstream

Private repo:

        cd azure-content-pr
        git remote add upstream https://[your GitHub user name]:[token]@github.com/Azure/azure-content-pr.git
        git fetch upstream

This usually takes a while. After you do this, you won't have to fork again or enter your credentials again. You would only have to copy the forks to a local computer again if you set the tools up on another computer.


## Configure your user name and email locally

To ensure you are listed correctly as a contributor, you need to configure your user name and email locally in Git.

1. Start Git Bash, and switch into azure-content or azure-content-pr:

   ````
   cd azure-content
   ````

 or

   ````
   cd azure-content-pr
   ````

2. Configure your user name so it matches your name as you set it up in your GitHub profile:

    ````
    git config --global user.name "John Doe"
    ````
3. Configure your email so it matches the primary email designated in your GitHub profile; if you're a MSFT employee, it should be your MSFT email address:

    ````
    git config --global user.email "alias@example.com"
    ````
4. Type `git config -l` and review your local settings to ensure the user name and email in the configuration are correct.

## Next steps

- [Create a local working branch](./git-commands-for-master.md) on your computer so you can start work
- If creating a new article, start with a copy of [the docs.microsoft.com markdown template](../template.md) 
- Back to [Step-by-step instructions](../readme.md#step-by-step) in main Contributor Guide

<!--Anchors-->
[Use a customer-friendly voice]: #use-a-customer-friendly-voice
[Consider localization and machine translation]: #consider-localization-and-machine-translation
[other style and voice issues to watch for]: #other-style-and-voice-issues-to-watch-for

[Create a GitHub account and set up your profile]: #create-a-github-account-and-set-up-your-profile
[Determine whether you really need to follow the rest of these steps]: #determine-whether-you-really-need-to-follow-the-rest-of-these-steps
[Permissions in GitHub]: #permissions-in-github
[Install Git for Windows]: #install-git-for-windows
[Enable two-factor authentication]: #enable-two-factor-authentication
[Install a markdown editor]: #install-a-markdown-editor
[Fork the repository and copy it to your computer]: #fork-the-repository-and-copy-it-to-your-computer
[Install git-credential-winstore]: #install-git-credential-winstore
[Sign up for Disqus]: #sign-up-for-disqus
[Configure your user name and email locally]: #configure-your-user-name-and-email-locally
[Next steps]: #next-steps
[Livefyre]: http://web.livefyre.com/
[DocsPubRepos]: ../readme.md#repository-organization
[UsingGithubEditor]: ../readme.md#minor-contributions-using-the-github-editor