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
If you get an error it is likely due to your computer not having Git.  Follow the instructions [here](https://happygitwithr.com/install-git.html) about installing Git

3. Set up your GitHub credentials on your computer.  Follow the instructions [here](https://happygitwithr.com/https-pat.html#tldr) about using `usethis::create_github_token()` and `gitcreds::gitcreds_set()` functions.  Also, save your GitHub PAT to a password manager so that you can find in the future (in case you need to interact with GitHub from a different computer).
4. Go to Canvas and get the link to accept the assignment.  Copy and paste the link in a web browser.  Accept the assignment.
5. Go to assignment at https://github.com/frec-3044.  Click on repository
6. Under the green "Code" button, select the local tab, and copy the https link.
7. Open Rstudio on your computer and create a new project. First, File -> New Project -> Version Control -> Git.  Paste the URL from you repo in the first box, hit tab to fill in the repo name in the second, and then use Browse to select where you want the project on your computer (I recommend having a directory on your computer where you keep all the assignments for the class).
8. Your project will load.  Then go to File -> New -> New File -> Rmarkdown... 
9. In the prompt use Title =  "Assignment 1" and Author = [Your name]
10. Save file as "assignment1.Rmd" in the **assignment subdirectory** of the Project.
11. Commit your Rmd file using the Git tab at the top right pane using a useful commit message. You will need to check the box for the files that you want to commit. A useful message helps you broadly remember what you did to the files that are included in the commit.  The Git tab may not be in the top right panel if you have moved the panels around.
9.  The top of your Rmd has options for the type of document it creates.  It should currently say "output=html_document".  Change the output to `output=github_document`
10. Knit (found on the top left pane) the document a to github_document.  You will see a file named "assignment1.md" appear.  This is a markdown file that GitHub can easy read and convert to nice looking text.
11. Commit the Rmd and md documents to git.
12. Push to your repository on GitHub.
13. Go to https://github.com/frec-3044 and click on your repository. Find your assignment1.md file and click on it.  It should look like a nicely formatted document.

If you are having issues (i.e., your compute does not seem to have Git installed), [here](https://happygitwithr.com/index.html) is an excellent resource to help you debug your git + Rstudio issues.
