## Introduction to GitHub, Git, and Quarto

1.  Test that you have Git on your computer. In RStudio, find the "Terminal" tab (likely bottom right panel, second tab) and type `git`.  If text that looks like help information appears, it means you have Git on your computer.  If not, then follow the instructions [here](https://happygitwithr.com/install-git.html) to install Git.  

2.  Create a GitHub user account at <https://github.com>, if you don't already have one. [Here is advice about choosing a user name](https://happygitwithr.com/github-acct.html#username-advice), because choosing a good user name is critical. You are *not* required to use your university email or an identifying username if you do not want to.

3.  Go to RStudio and install the `usethis` package.

```         
install.packages("usethis")
```

4.  Run the following command, where you replace the user.email and user.name with the email used for GitHub and your GitHub user name. You can learn more about the command [here](https://happygitwithr.com/hello-git.html#hello-git)

```         
library(usethis)
use_git_config(user.name = "Jane Doe", user.email = "jane@example.org")
```

5.  Set up your GitHub credentials on your computer. Follow the instructions [here](https://happygitwithr.com/https-pat.html#tldr).

You will use `usethis::create_github_token()` `gitcreds::gitcreds_set()` functions. 

The `usethis::create_github_token()` command will take you to GitHub, where you create a token.  

**IMPORTANT: When creating your GitHub token, be sure your GitHub PAT doesn't expire before the end of the semester.**

Copy the token to your clipboard and then run `gitcreds::gitcreds_set()`.  When prompted in the R console to enter your token, paste it from your clipboard,

Also, save your GitHub PAT in a password manager so you can find it later (in case you need to interact with GitHub from a different computer).

6.  Go to Canvas and get the link to accept the assignment. Copy and paste the link into a web browser. Accept the assignment.  You may need to check your email for a confirmation email from GitHub that you want to join the GitHub Classroom associated with the class.  This email is different from an email about accepting the assignment.

7.  Go to your assignment at <https://github.com/frec-3044-Spring26>. Click on the repository.

8.  Under the green "Code" button, select the local tab and copy the https link.

9.  Open RStudio on your computer and create a new project. First, File -\> New Project -\> Version Control -\> Git. Paste the URL from your repo into the first box, hit tab to fill in the repo name in the second, and then use Browse to select where you want the project on your computer (I recommend creating a directory on your computer where you keep all the repositories we use in the class).

10.  Your project will load. Then go to File -\> New -\> New File -\> Quarto Document

11. In the prompt use Title = "Assignment 1" and Author = [Your name]

12. Save file as "assignment1.qmd" in the **assignment subdirectory** of the Project.

13. Commit your `assignment1.qmd` file using the Git tab at the top right pane using a helpful commit message. You will need to check the box in the "staged" column for the files that you want to commit. A window will pop up where you can provide a helpful message to help you quickly remember what you did to the files included in the commit. The Git tab may not appear in the top-right panel if you have moved the panels around.

14. Find the Sources / Visual buttons right above the document. Select Source (which is the code view).

15. Add this to the end of the qmd document.  Be sure to include the beginning"```{r}" and the end "```" when you copy and paste.

```{r}
plot(cars$speed, cars$dist)
```

16.  Add your GitHub username to the bottom of your qmd document (I need this to compare your submitted assignment to your GitHub repo)

17. Find the following code at the top of your qmd file.

```         
format: html:
```

and change it so that all the necessary files are saved in a single HTML file.

```         
format:   
  html:
    embed-resources: true
```

18. Find the Render button (found above the document)  and click it to render the document to HTML. You will see a file named "assignment1.html" appear. HTML is like a webpage version of your code. If you have a directory called `assignment1_files,` then you did not do step 17 correctly.
19. Click on the "assignment1.html" in your "Files" pane and select "View in Web Browser". Confirm that it looks as expected.
20. Commit the updated `.qmd` and new `.html` files to git.
21. Push to your repository on GitHub. The Push button is near the Commit button in the Git Panel.
22. Go to <https://github.com/frec-3044-Spring26> and click on your repository. You should also see 3-4 commits: 2 were committed by you and 1-2 by the GitHub Classroom bot. The GitHub Classroom bot commit is the automatic commit that occurred when you accepted the assignment.
23. Go to the course on Canvas and upload the .html file to the assignment.

If you are having issues (e.g., your computer does not seem to have Git installed), [here](https://happygitwithr.com/index.html) is an excellent resource for debugging your git + RStudio issues.
