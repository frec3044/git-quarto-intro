## Introduction to Github, Git, and Rmarkdown

1.  Create a GitHub user account at <https://github.com>, if you don't already have one. [Here is advice about choosing a user name](https://happygitwithr.com/github-acct.html#username-advice), because choosing a good user name is critical. Please email me your user name so I can associate it with your name in the grade book.

2.  Go to Rstudio and install the `usethis` package.

```         
install.packages("usethis")
```

3.  Run the following command where you replace the user.email and user.name with the email used for GitHub and your GitHub user name. You can learn more about the command [here](https://happygitwithr.com/hello-git.html#hello-git)

```         
library(usethis)
use_git_config(user.name = "Jane Doe", user.email = "jane@example.org")
```

If you get an error at this step, it is likely due to your computer not having Git. Follow the instructions [here](https://happygitwithr.com/install-git.html) about installing Git

4.  Set up your GitHub credentials on your computer. Follow the instructions [here](https://happygitwithr.com/https-pat.html#tldr) about using `usethis::create_github_token()` and `gitcreds::gitcreds_set()` functions. Also, save your GitHub PAT to a password manager to find it in the future (in case you need to interact with GitHub from a different computer).

5.  Go to Canvas and get the link to accept the assignment. Copy and paste the link in a web browser. Accept the assignment.

6.  Go to your assignment at <https://github.com/frec-3044-Spring25>. Click on the repository.

7.  Under the green "Code" button, select the local tab and copy the https link.

8.  Open Rstudio on your computer and create a new project. First, File -\> New Project -\> Version Control -\> Git. Paste the URL from your repo in the first box, hit tab to fill in the repo name in the second, and then use Browse to select where you want the project on your computer (I recommend having a directory on your computer where you keep all repositories we use in the class).

9.  Your project will load. Then go to File -\> New -\> New File -\> Quarto Document

10. In the prompt use Title = "Assignment 1" and Author = [Your name]

11. Save file as "assignment1.qmd" in the **assignment subdirectory** of the Project.

12. Commit your `assignment1.qmd` file using the Git tab at the top right pane using a helpful commit message. You will need to check the box in the "staged" column for the files that you want to commit. A window will pop up where you provide a helpful message that helps you quickly remember what you did to the files included in the commit. The Git tab may not be in the top right panel if you have moved the panels around.

13. Find the Sources / Visual buttons right above the document. Select Source (which is the code view).

14. Copy the code chunk on lines 21-24 and paste it at the end of the document. Change to `echo: TRUE`.

15. Find the following code at the top

```         
format: html:
```

and change it so that all the necessary files are saved in a single html file.

```         
format:   
  html:
    embed-resources: true
```

16. Find the Render (found above the document) button and click it to render the document to HTML. You will see a file named "assignment1.html" appear. HTML is like a webpage version of your code. If you have a directory called `assignment1_files,` then you did not do step 15 correctly.
17. Click on the "assignment1.html" in your "Files" pane and select "View in Web Browser". Confirm that it looks as expected.
18. Commit the updated `.qmd` and new `.html` files to git.
19. Push to your repository on GitHub. The Push button is near the Commit button in the Git Panel.
20. Go to <https://github.com/frec-3044-Spring25> and click on your repository. You should also see three commits: 2 were committed by you, and 1 was committed by the GitHub classroom bot. The Github classroom bot commit is the automatic commit that occurred when you accepted the assignment.
21. Go to the course on Canvas and upload the .html file to the assignment.

If you are having issues (e.g., your computer does not seem to have Git installed), [here](https://happygitwithr.com/index.html) is an excellent resource for debugging your git + Rstudio issues.
