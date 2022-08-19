# Contributing to Re3gistry software

Thank you for your interest in contributing to the Re3gistry project. We would appreciate it if you would read this information carefully so that we can propagate your changes as soon as possible.

Please read and follow our [Code of Conduct](CODE_OF_CONDUCT.adoc) before you start interacting with the Re3gistry community.


We distinguish between two types of changes to the R3TF software that are handled differently:

* For changes that provide bug fixes a Pull Request can be created that references an existing bug in the R3TF repository.
* Changes that provide improvements to the software must first be discussed in an Re3gistry Improvement Proposal (R3IP) and reference an accepted R3IP.

Your Pull Request will be reviewed by the managers of the repository.


## Developer Certificate of Origin
Registry software is Licensed under the [European Public License 1.2](https://opensource.org/licenses/EUPL-1.2). For all project contributions it is necessary to follow the Developer Certificate of Origin (DCO) mechanism.

The DCO is legally binding statement that ensures you are the creator of the contribution, and that you allow the Re3gistry project to use your work. The Developer Certificate of Origin can be found at [http://developercertificate.org/](http://developercertificate.org/).

The DCO is attached to every contribution made by every developer. In the commit message of the contribution, the developer must add a `Signed-off-by` statement to agree to the DCO and digitally sign it with a GPG signature.

Please refer to both sources to learn how to configure and use your GIT:
* [https://git-scm.com/docs/git-commit#git-commit---signoff](https://git-scm.com/docs/git-commit#git-commit---signoff)
* [https://help.github.com/articles/signing-commits/](https://help.github.com/articles/signing-commits/)

Most GIT clients support adding `Signed-off-by` to the commit messages but do not support the configuration of signing the commits with GPG. Please check if the settings for user, commit and gpg are set in your local GIT configuration. An example:
      
```
[user]
  name = John Doe
  email = deo@whatever.com
  signingkey = 420A420FFF
[commit]
  gpgsign = true
[gpg]
  program = /usr/local/bin/gpg
```

## Changes to the Re3gistry software
We distinguish between two types of changes to the Re3gistry software that are handled differently:
* For changes that provide **bug fixes** a Pull Request can be created that references an existing bug in the [Registry repository](https://github.com/ec-jrc/re3gistry/issues). Steps to follow:
    * If you would like to submit a bug report, please create a new issue in the re3gistry repository using the [Bug report template](https://github.com/ec-jrc/re3gistry/issues/new?assignees=&labels=&template=re3gistry-problem.md). The Re3gistry Technical Committee members monitor the issues and will add new label to the issue. If additional information is required, you will be contacted.
    * Pull requests for bugfixes are very welcome (see "Contributing" below)!
* Changes that provide **improvements** to the software must first be discussed in an [Registry Improvement Proposal](https://github.com/ec-jrc/re3gistry/issues/new?assignees=&labels=&template=re3gistry-improvement-proposal.md) (R3IP) and reference an accepted R3IP. Steps to follow:
    * If you would like to discuss an idea before documenting a full R3IP, simply create a new issue using the [R3IP template](https://github.com/ec-jrc/re3gistry/issues/new?assignees=&labels=&template=re3gistry-improvement-proposal.md). Complete the template as far as possible and mention that this is not a complete proposal yet, but that you are looking for feedback. The R3TF Group members monitor the issue and if they support it, it will change the tag to "approved" and ask you to complete the proposal.
    
    
## Pull Request Workflow
* Please read and accept the Developer Certificate of Origin. All commits have to be **signed-off** and **digitally signed**. Make sure you have configured your GIT client accordingly.
* Fork the repository
    * Navigate to the Re3igstry project at https://github.com/ec-jrc/re3gistry
    * Click **FORK**
    * GitHub will take you to your own copy/fork of the Re3gistry repository
* Clone a fork

   You've successfully create a Re3gistry repository which only exists on GitHub. To be able to work on the project you need to clone it in your computer.
     * In GitHub navigate to **your fork** of the Re3gistry repository
     * Above the list of files, click **Code**
     * Copy the URL for the repository
     * Open Git Bash or your favorite Git tool
     * Change the working directory to the directory where you want to clone
     * Type `git clone` and the URL you have copied in one of the previous steps. 
     `git clone https://github.com/your_username/re3gistry`
     * Press *Enter* and your local clone will be created.
     * Create a branch:
         * Navigate to your local repository
         * Check that your fork is the "origin" remote
         * Add the project repository as the "upstream remote"
         * Pull the latest changes from upstream into your local repository
         * Create a new branch
         Use `git checkout -b branch_name` to create a new branch and than immediately switch to it. 
         The branch name should be 'R3IP-NUMBER' for an Re3gistry Improvement Proposal, where NUMBER is the GitHub issue number from governance repository or 'bug-NUMBER' where NUMBER is the GitHub issue number from the Re3gistry repository.
* Making and pushing changes

   Start adding your code. When you're ready to submit your changes, stage and commit your changes. 
   * Use `git add .` to tell Git that you want to inlude all your changes in the next commit and 
   * use `git commit` to take a snapshot of your changes. 
   `git commit -m "short description of the changes"`. You can do as many commits as you wish. 
   * But when you are ready with your code push your changes to the remote `git push`

## Making a Pull Request
* A Pull Request can be composed by one or multiple commits. All changes together address one high-level concern. If a Pull Request provides multiple, distinct features from different sections and each section addresses a separate concern, without addressing one common high-level concern, it will be rejected. Examples for bad Pull Requests: a Pull Request that provides a bugfix and adds a feature or a Pull Request that addresses multiple R3IPs.
* Changes must be traceable in the commit history.
* Make sure you have added Javadocs if you have added public interfaces.
* Make sure there are no commented out code sections.
* English language needs to be used in the code and comments.


* Create the Pull Request
   When opening a "pull request", you are making a "request" that the project repository "pull" changes from your fork. You will see that the project repository is listed as the "base repository", and your fork is listed as the "head repository"
* Review the Pull Request
* You can add more commits to your pull request
   You can continue to add commits to your Pull Request even after opening it. For example: the project maintainers may ask you to make some more changes or you may want to include something that you forgot.
* Discuss the Pull Request   
   You can use the comment box to at the bottom of the Pull Request to address questions that the project maintainer might have
