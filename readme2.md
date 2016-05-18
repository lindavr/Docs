title: Docs.microsoft.com contributor guide
description:
keywords:
author: bryanla
manager: 
ms.date: 05/17/2016
ms.topic: article
ms.prod:
ms.service: 
ms.technology:
ms.assetid: 6EFEA410-29E0-400C-A1C2-D93296DDD1DD


# Docs.microsoft.com contributor guide

Thank you for your interest in [docs.microsoft.com](https://docs.microsoft.com/), home of the technical content for products and services from Microsoft's Cloud and Enterprise Division!

This is the main page of the Contributor Guide, which is broken into the following sections:

* [How to contribute](#how-to-contribute) - covers the various ways you can contribute, not only to the content, but to the larger communities that use services and features covered by docs.microsoft.com content.
  * [Pull Request overvew](#pull-request-overview) - since the Pull Request mechanism is a primary way in which all content contributions are made, this section provides a brief overview of the process, which sets context for the following sections.
  * [Minor corrections: using the GitHub editor](#minor-corrections-using-the-GitHub-editor) - provides details on one of the two ways you can contribute to content, mainly for small contributions such as corrections.
  * [Large submissions: using a fork](#large-submissions-using-a-fork) - provides details on the second way in which you can contribute to content, when you need to make more than just minor contributions, which is where the majority of the Contributor Guide is focused.
* test

## How to contribute

You can contribute to docs.microsoft.com content and community in a few different ways:

* **Submit feedback/questions** directly in a [docs.microsoft.com](https://docs.microsoft.com/) article. There are 2 ways of doing this, both of which require you to first sign in to Livefyre ([sign up](https://livefyre.zendesk.com/hc/en-us/articles/200329426-How-do-I-create-a-Livefyre-Account-) with an existing social account, or create a Livefyre account using a designated email address) :
  * General comments can be provided by using the "Comments" feature at the bottom of the article page
  * Context-specific comments can be embedded in the related section/paragraph, by hovering the text and clicking the "sidenote" caption icon
* **Participate in community discussion**, such as a [Microsoft forum][Forum-MSDN-Main] or [Stack Overflow][Forum-SO-Main] discussion. See the [Repository organization](#repository-organization) section below for service-specific examples.
* **Submit a Pull Request**, which contains your suggested changes to the actual content, targeting content in one of the docs.microsoft.com GitHub repositories. See the [Repository organization](#repository-organization) section below for the list of repositories.

The remainder of this article is devoted to the last option, and provides additional detail on how you can use the GitHub Pull Request feature to make contributions. 

## Contributing via Pull Request

GitHub is a hosting service for Git repositories, which is where docs.microsoft.com content is stored. A Git *repository* (aka: *repo*) is a conceptual container for one or more branches. A *branch* contains the actual folders/files that make up the set of content for a project. Branches and can also be used for versioning, with the 'master' branch serving as the main plan-of-record for the project.

A *Pull Request* provides a convenient way to bundle up a series of proposed changes (aka: *commits*) stored in a contributor's source branch, allowing GitHub to first model the changes that would occur if they were *merged* in the target 'master' branch, then eventually merge them. A Pull Request also serves as a mechanism for you and the Pull Request reviewer to have a conversation about the changes if necessary, and cover any potential questions or issues before the changes on the source branch are merged into the target branch. 

There are a couple of different ways of contributing via Pull Request, depending on the size of changes you would like to propose.

### Minor corrections: using the GitHub editor

If you're looking for a quick way to make a minor contribution, you can do this directly in the GitHub Web page that corresponds to the file in which you would like to propose changes. This requires little/no knowledge of Git versioning workflow, and you can start this process by using either of the following methods :

* visit the specific article on [https://docs.microsoft.com/](https://docs.microsoft.com/),  then click the "Edit" link in the upper-right corner of the article  
* find the article by browsing the Markdown files in the related repository (see below for the list)  
 
Both of these will allow you to navigate directly into the GitHub page that serves the article source. Once you are there, click the "Edit" pencil icon in the upper right to go into edit mode. Here you can specify your changes using the GitHub file editor. 

When you're finished, scroll to the bottom of the page where you can "Propose file change", which is the default option when you have read access to the repository. Users with read access will then be directed to a working branch in their own fork of the repository (which GitHub will also create for you if it does not already exist), and be presented with a "Create pull request" page to create a new entry in the repo's Pull Request queue. For more information, see the [Editing files in another user's repository](https://help.github.com/articles/editing-files-in-another-user-s-repository/) GitHub article.

**Note**: the workflow is slightly different when you have write permissions to a repository. For more information, see the [Editing files in your repository](https://help.github.com/articles/editing-files-in-your-repository/) GitHub article.

### Large submissions: using a fork

If you are making substantial changes to an existing article, adding or changing images, or contributing a new article, you will need to fork the repository you will be contributing to, using the GitHub user interface. A fork is a replica of the main repository, which provides you with a working copy which you can use in isolation. If you're not already familiar with making Github contributions, you will also need to install a local Git tool such as Git Bash, a Markdown editor, and learn some Git commands. 

### Additional considerations

* If you submit a pull request with new files or significant changes to documentation or code samples, we may also need to correspond with you in the pull request, asking you to submit an online Contribution License Agreement (CLA).
* Minor corrections or clarifications you submit for documentation and code examples in the repository are covered by the [Microsoft Terms of Use (ToU)](https://www.microsoft.com/en-us/legal/intellectualproperty/copyright/default.aspx).
* If you are a Microsoft employee please always make your contributions via a fork, and use the internal repository. This will ensure your contributions run through the build validation process, and afford you a staging environment for evaluating/testing your changes.
*  See the [Resources](#resources) section below for more information on Git concepts such as repositories, forks, branches, pull requests, etc.  

## Repository organization

The content published to docs.microsoft.com is partitioned into several GitHub repositories. The table below enumerates the current set of docs.microsoft.com landing pages, the GitHub repository that contains the associated articles, and the related discussion forum(s) :

| Main Landing Page | Solution/Service Landing Page | GitHub Org/Repository | Discussion Forum(s) |
|:---------------------------:|:-------------------------------------------:|:-------------------------:|:----------------------------:|
| [Enterprise Mobility][EM-Land-Page] |     | [Microsoft/EMDocs][EM-Land-Repo] | [MSDN][Forum-MSDN-EM] |
|     | [Azure Active Directory][EM-AzureAD-Land] | [Azure/Azure-Content][EM-AzureAD-Repo] | [MSDN][Forum-MSDN-AzureAD], [Stack Overflow][Forum-SO-AzureAD] |
|     | [Multi-Factor Authentication][EM-MFA-Land] | [Azure/Azure-Content][EM-MFA-Repo] | [MSDN][Forum-MSDN-MFA], [Stack Overflow][Forum-SO-MFA] |
|     | [Microsoft Identity Manager][EM-MIM-Land] | [Microsoft/MIMDocs][EM-MIM-Repo] | [MSDN][Forum-MSDN-MIM], [Stack Overflow][Forum-SO-MIM] |
|     | [Microsoft Intune][EM-Intune-Land] | [Microsoft/IntuneDocs][EM-Intune-Repo] | [MSDN][Forum-MSDN-Intune], [Stack Overflow][Forum-SO-Intune] |
|     | [Azure Rights Management][EM-AzureRMS-Land] | [Microsoft/Azure-RMSDocs][EM-AzureRMS-Repo] | [MSDN][Forum-MSDN-AzureRMS], [Stack Overflow][Forum-SO-AzureRMS] |
|     | [Microsoft Advanced Threat Analytics][EM-ATA-Land] | [Microsoft/ATADocs][EM-ATA-Repo] | [MSDN][Forum-MSDN-ATA] |
|     | [Azure RemoteApp][EM-RemoteApp-Land] | [Azure/Azure-Content][EM-RemoteApp-Repo] | [MSDN][Forum-MSDN-RemoteApp], [Stack Overflow][Forum-SO-RemoteApp] |

The content in each repository is loosely aligned with the organization of the articles on the corresponding [https://docs.microsoft.com/](https://docs.microsoft.com/) landing pages. A series of subdirectories are used for separation of usage scenarios/stages (ie: Understand & Explore, Deploy & Use, etc), along with media content (ie: image files) and include files (Markdown files that are reused across multiple main articles).

### Main articles directory

The main articles directory is found directly off the root of the repository, and contains a set of subdirectories with articles formatted as Markdown files with an *.md* extension. For example, the IntuneDocs repository content is the `\InTuneDocs` subdirectory. 

Within the root of this directory are general articles that relate to the overall service, along with another series of subdirectories, which match the common scenarios as outlined on the main landing page for the service. For instance, the Intune "Understand & Explore" articles are in the `Understand` subdirectory, "Deploy & Use" articles are found in the `DeployUse` subdirectory, etc.  

* **Article filenames:** Note that filenames use the following rules:
    * Contain only lowercase letters, numbers, and hyphens. 
    * No spaces or punctuation characters. Use the hyphens to separate words and numbers in the file name.
    * No more than 80 characters - this is a publishing system limit
    * Use action verbs that are specific, such as develop, buy, build, troubleshoot. No -ing words.
    * No small words - don't include a, and, the, in, or, etc.
    * Must be in Markdown and use the .md file extension. 
* **Media subdirectory:** As mentioned, each article directory also contains a `\media` subdirectory for corresponding media files, inside which are images used by articles that have image references.  
* **Includes subdirectory:** Whenever we have reusable content that is shared across two or more articles, it is placed in an `includes` subdirectory off of the main articles directory. In the Markdown file that wishes to use the include file, a corresponding INCLUDE Markdown extension is placed in the location where the include file needs to be referenced.  

     The format of the extension is as follows:

    `> [!INCLUDE[accessibility6](./includes/accessibility6_md.md)]`

    The statement must begin with `> [!INCLUDE`, followed immediately by a user-defined name for the include site enclosed in brackets, `[accessibility6]`, followed immediately by the relative path to the include file enclosed in parentheses, `(./includes/accessibility6_md.md)`, and terminated with the closing bracket, `]`.

### Markdown file template

For convenience, the root directory of each repository contains a Markdown template file named `template.md`, which can be used as a "starter file" if you need to create a new article for submission to the repository. The file contains various examples of using Markdown to format an article, along with general instructions. 

At the top of the file, you'll also see a "metadata" section, which contains various tags used for tracking information relating to the article. Article metadata enables certain functionality, such as author attribution, contributor attribution, breadcrumbs, article descriptions, and SEO optimizations as well as reporting Microsoft uses to evaluate the performance of the content. So the metadata is important! If you're unsure of the values to use for the metadata section, you can leave them blank and they will be reviewed/completed by the pull request reviewer for the repository.

## Using a GitHub fork to make contributions

As mentioned earlier, if you are making large contributions or are a Microsoft employee, you will need to make your contributions via a GitHub fork. If you're unfamiliar with Git, you may want to review some of the resources provided in the [Resources](#resources) section below.

### Quickstart
Once you've configured your GitHub account, installed a client Git tool (such as [Git Bash](https://git-scm.com/downloads)), and created your own fork of the repository, you can used the following general steps to start contributing to this repo:

1.Clone the repository:  


    git clone https://github.com/Microsoft/IntuneDocs.git

2.Create a branch for your local work.  
3.Edit the Markdown files using your favorite Markdown editor.  
4 Commit and push your changes back up to your forked repository:  
        
        git add -u
        git commit -m "update doc"
        git push  
          
5.Return to GitHub and create a pull request, requesting that your branch be pulled into the "master" branch of the related Enterprise Mobility repository.  
6. Your content will be automatically published once the pull request is accepted.  

### Branches

We recommend that you create local working branches that target a specific scope of change. Each branch should be limited to a single concept/article both to streamline work flow and reduce the possibility of merge conflicts.  The following efforts are of the appropriate scope for a new branch:

* A new article (and associated images)
* Spelling and grammar edits on an article.
* Applying a single formatting change across a large set of articles (e.g. new copyright footer).

## Resources

### GitHub/Git

* If you're unfamiliar with Git, you may want to first review some [basic Git terminology](https://help.github.com/articles/github-glossary). In addition, [this StackOverflow thread](http://stackoverflow.com/questions/7076164/terminology-used-by-git.) contains a glossary of Git terms you'll encounter in this set of steps.
* The [Learn Git course by Codecademy](https://www.codecademy.com/learn/learn-git) provides a 2 hour introduction to Git
* The free [Pro Git e-book](http://git-scm.com/book/en/v2) provides excellent depth if you are new to Git, and also serves as a good reference
* See the [Git Bash downloads page](https://git-scm.com/downloads) for the available Git Bash downloads by platform. Git Bash provides you with the tools you will need for proposing larger contributions via a personal fork of the repository, as discussed above.

### Markdown
All the articles in this repository use GitHub flavored Markdown. See [Markdown basics](https://help.github.com/articles/getting-started-with-writing-and-formatting-on-github/) for a good reference on getting started, and the [GitHub Markdown Cheatsheet](https://guides.github.com/pdfs/markdown-cheatsheet-online.pdf) for a handy syntax reference. 

This is not an exhaustive list, but here are a few ideas for Markdown editors that you may wish to try:

- **Atom**: GitHub's Atom Markdown editor: [http://atom.io](http://atom.io). It does not require a license for business use. It has spell check. 
- **Prose**: This is a lightweight, elegant, on-line, and open source Markdown editor that offers a preview. Visit [http://prose.io](http://prose.io) and authorize Prose in your repository.
- **[Visual Studio Code](https://www.visualstudio.com/products/code-vs.aspx)** - A lightweight but powerful source code editor which runs on your desktop and is available for Windows, OS X and Linux. 
- **Notepad**: You can use Notepad for a very lightweight option.



<!---- Reference links for Docs landing pages, associated GitHub repositories, and related Forums matrix. ------------------>
<!---- PLEASE INSERT URLS IN ASCENDING SORT ORDER, AND REMOVE LOCALE SEGMENT FROM URLS (ie: en-us) FOR LOCALIZED FORUMS! -->
[EM-ATA-Land]: https://docs.microsoft.com/advanced-threat-analytics/
[EM-ATA-Repo]: https://github.com/Microsoft/ATADocs
[EM-AzureAD-Land]: https://docs.microsoft.com/active-directory/
[EM-AzureAD-Repo]: https://github.com/Azure/azure-content/tree/master/articles/active-directory/
[EM-AzureRMS-Land]: https://docs.microsoft.com/rights-management/
[EM-AzureRMS-Repo]: https://github.com/Microsoft/Azure-RMSDocs
[EM-Intune-Land]: https://docs.microsoft.com/intune/
[EM-Intune-Repo]: https://github.com/microsoft/intuneDocs
[EM-Land-Page]: https://docs.microsoft.com/enterprise-mobility/
[EM-Land-Repo]: https://github.com/Microsoft/EMDocs/
[EM-MFA-Land]: https://docs.microsoft.com/multi-factor-authentication/
[EM-MFA-Repo]: https://github.com/Azure/azure-content/tree/master/articles/multi-factor-authentication
[EM-MIM-Land]: https://docs.microsoft.com/microsoft-identity-manager/
[EM-MIM-Repo]: https://github.com/Microsoft/MIMDocs
[EM-RemoteApp-Land]: https://docs.microsoft.com/en-us/remoteapp/
[EM-RemoteApp-Repo]: https://github.com/Azure/azure-content/tree/master/articles/remoteapp

[Forum-MSDN-ATA]: https://social.technet.microsoft.com/Forums/en-US/home?forum=mata
[Forum-MSDN-AzureAD]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=WindowsAzureAD
[Forum-MSDN-AzureRMS]: https://social.technet.microsoft.com/Forums/en-US/home?forum=rmscloud
[Forum-MSDN-EM]: https://social.technet.microsoft.com/Forums/en-US/home?sort=relevancedesc&brandIgnore=True&searchTerm=Enterprise+Mobility
[Forum-MSDN-Intune]: https://social.technet.microsoft.com/Forums/en-us/home?category=microsoftintune
[Forum-MSDN-Main]: https://social.technet.microsoft.com/Forums/home
[Forum-MSDN-MFA]: https://social.msdn.microsoft.com/Forums/en-US/home?forum=windowsazureactiveauthentication
[Forum-MSDN-MIM]: https://social.technet.microsoft.com/Forums/en-US/home?category=identitymanagement
[Forum-MSDN-RemoteApp]: https://social.technet.microsoft.com/Forums/en-US/home?filter=alltypes&brandIgnore=True&sort=relevancedesc&searchTerm=Azure+Remote+or+RemoteApp
[Forum-SO-AzureAD]: http://stackoverflow.com/questions/tagged/azure-active-directory
[Forum-SO-AzureRMS]: http://stackoverflow.com/questions/tagged/rights-management
[Forum-SO-Main]: http://stackoverflow.com/tags
[Forum-SO-Intune]: http://stackoverflow.com/questions/tagged/intune
[Forum-SO-MFA]: http://stackoverflow.com/search?q=%5Bazure%5D+multi-factor
[Forum-SO-MIM]: http://stackoverflow.com/search?q=Microsoft+Identity+Manager
[Forum-SO-RemoteApp]: http://stackoverflow.com/questions/tagged/remoteapp

