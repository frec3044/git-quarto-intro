## Introduction to Github, Git, and Rmarkdown

1. Create a GitHub user account at https://github.com, if you don't already have one.  [Here is advice about choosing a user name](https://happygitwithr.com/github-acct.html#username-advice), because choosing a good user name is critical.
2. Go to Rstudio and install the `usethis` package. 
```
install.packages("usethis")
```
3. Run the following command where you replace the user.email and user.name with the email used for GitHub and your GitHub user name.  You can learn more about the command [here](https://happygitwithr.com/hello-git.html#hello-git)
```
library(usethis)
use_git_config(user.name = "Jane Doe", user.email = "jane@example.org")
```
3. Set up your GitHub creditials on your computer.  Follow the instructions [here](https://happygitwithr.com/https-pat.html#tldr) about using `usethis::create_github_token()` and `gitcreds::gitcreds_set()` functions.  Also, save your GitHub PAT to a password manager so that you can find in the future (in case you need to interact with GitHub from a different computer).
4. Go to Canvas and get the link to accept the assignment.  Copy and paste the link in a webbrowser.  Accept the assignment.
5. Go to assignment at https://github.com/frec-3044.  Click on repository
6. Under the green "Code" button, select the local tab, and copy the https link.
7. Open Rstudio on your computer and create a new project. First, File -> New Project -> Version Control -> Git.  Paste the URL from you repo in the first box, hit tab to fill in the repo name in the second, and then use Browse to select where you want the project on your computer (I recommend having a directory on your computer where you keep all the assignments for the class).
8. Your prject will load.  Then go to New -> New File -> Rmarkdown... 
9. In the prompt use Title =  "Assignment 1" and Author = [Your name]
10. Save file as "assignment1.Rmd" in the assignment subdirectory of the Project.
11. Commit to your Rmd file using the Git tab at the top right pane using a useful commit message. You will need to check the box for the files that you want to commit. A useful message helps you broadly remember what you did to the files that are included in the commit.
9.  Change output to `github_document`
10. Knit (found on the top left pane) the document a to github_document
11. Commit the Rmd and md documents to git.
12. Push to your repository on GitHub.  You will be prompted for your user name (or email) and your password.

If you are having issues (i.e., your compute does not seem to have Git installed), [here](https://happygitwithr.com/index.html) is an excellent resource to help you debug your git + Rstudio issues.
