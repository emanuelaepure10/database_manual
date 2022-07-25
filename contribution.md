# Contributing to Re3gistry software

Thank you for your interest in contributing to the Re3gistry project. We would appreciate it if you would read this information carefully
## Before you start

* Do you want to setup your own repository using Re3gistry codebase?
* Do you want to develop a big feature on top of this codebase? Or do you want to solve a bug you or someone else have found?
* Do you have problems in installing the project?
* Or you just want to report an issue?

Please us the GitHub issues to get in touch with us! And lt us know about your plans.

## Legal
Please read and follow our Code of Conduct ??? before you start interacting with the Re3gistry community.

## Developer Certificate of Origin
Registry software is Licensed under the [European Public License 1.2](https://opensource.org/licenses/EUPL-1.2). For all project contributions it is necessary to follow the Developer Certificate of Origin (DCO) mechanism.
To Complete!!!

## Changes to the Re3gistry software
We distinguish between two types of changes to the Re3gistry software that are handled differently:
* For changes that provide **bug fixes** a Pull Request can be created that references an existing bug in the [Registry repository](https://github.com/ec-jrc/re3gistry/issues) 
* Changes that provide **improvements** to the software must first be discussed in an [Registry Improvement Proposal](https://github.com/ec-jrc/re3gistry/issues/new?assignees=&labels=&template=re3gistry-improvement-proposal.md) and reference an accepted.

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
* Making and pushing changes

   Start adding your code. When you're ready to submit your changes, stage and commit your changes. 
   * Use `git add .` to tell Git that you want to inlude all your changes in the next commit and 
   * use `git commit` to take a snapshot of your changes. 
   `git commit -m "short description of the changes"`. You can do as many commits as you wish. 
   * But when you are ready with your code push your changes to the remote `git push`

## Making a Pull Request
      * A Pull Request can be composed by one or multiple commits. All changes together should address one single issue. 
      The pull request will not be accepted if it is addressing more than one concern. 
      Example of Bad Pull Request: a Pull Request that provides a bugfix for the backend and an improvement for the webapp.
      * Changes must be traceable in the commit history.
      * Make sure you have added Javadocs if you have added public interfaces.
      * Make sure there are no commented out code sections.
      * English language needs to be used in the code and comments.
* *Create* the Pull Request
   When opening a "pull request", you are making a "request" that the project repository "pull" changes from your fork. You will see that the project repository is listed as the "base repository", and your fork is listed as the "head repository"
* *Review* the Pull Request
* You can *add more commits* to your pull request
   You can continue to add commits to your Pull Request even after opening it. For example: the project maintainers may ask you to make some more changes or you may want to include something that you forgot.
* *Discuss* the Pull Request   
   You can use the comment box to at the bottom of the Pull Request to address questions that the project maintainer might have
