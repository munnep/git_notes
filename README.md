# Git notes

# Summary
This documentation describes the exercise for git training

# Exercise 1: Create a repository

## Goal
- create a new repository

1. login to your github account account  
[https://github.com/](https://github.com/)
1. On the left side repository click on **new**   
![](media/2021-10-13-12-06-06.png)
3. Fill in the following things
- Reposity name: **avengers**
- Description: **avengers example**
- choose **Public**
- Iinitialize the repository with 
  - **Readme file** 
  - choose a license -> **MIT license**  
![](media/2021-10-13-12-10-17.png)  
Click create repository 
4. You should see a repository called avengers  
![](media/2021-10-13-12-14-35.png)  

# Exercise 2: Merge a branch

## Goal
- create a branch - feature release
- make a change to the readme file
- create a pull request
- merge into into the main branch 

## steps
1. Go to your repository
![](media/2021-10-13-12-29-18.png)  
2. go to the main and switch branch and enter **feature release** and click on the Create branch: feature release
![](media/2021-10-13-12-31-44.png)  
3. check that you are on the feature-release branch now
![](media/2021-10-13-12-32-33.png)  
4. Change something in the readme file by click on the pencil
![](media/2021-10-13-12-33-29.png)  
5. make some changes and go to the bottom 
6. With the commit changes. Write a description of what you changed and commit directly to the feature-release branch button  
![](media/2021-10-13-12-36-38.png)
7. Click the Commit changes button
8. You now want to merge this change to the main branch
9. Click on the Pull Requests  
![](media/2021-10-13-12-39-00.png)  
10. We want to merge the feature-release branch into the main release. Check that it is now like this
![](media/2021-10-13-12-40-50.png)  
11. Give it some clear explanation and write something description. Click the **Create Pull request**
![](media/2021-10-13-12-42-08.png)  
12. You can now merge the pull request. Click on it
![](media/2021-10-13-12-43-03.png)  
13. Confirm the merge request  
![](media/2021-10-13-12-43-36.png)  
14. Delete the feature-release branch. Click on it
![](media/2021-10-13-12-44-21.png)  
15. Check the results
- You only have the main branch
- You see the change of the README.md you made
![](media/2021-10-13-12-45-39.png)   


# Exercise 3: Create a organization

## Goal
- create an organization 

## steps
1. login to your github account account  
[https://github.com/](https://github.com/)
2. On the top right side go to your profile and go to **settings**
![](media/2021-10-13-13-44-43.png)
3. On the left go to organizations
![](media/2021-10-13-13-45-20.png)
4. Select New organization  
![](media/2021-10-13-13-45-47.png)  
5. select a Free account
![](media/2021-10-13-13-46-19.png)  
6. Set up your organization  
- organization account name: **superheroes-munnep**
- Contact email: **patrick.munne@hashicorp.com**
- This organization belongs to: **My personal account**  
![](media/2021-10-13-13-48-53.png)  
7. Complete the setup
![](media/2021-10-13-13-49-40.png)  
8. Confirm your login credentials
9. Now you should have **Your Organizations** under your username on the top right side
![](media/2021-10-13-13-51-36.png)  
10. See an overview of your organization
![](media/2021-10-13-13-52-33.png)  
11. You have an organization 
![](media/2021-10-13-13-53-07.png)  

# exercise 4

## Goal
- create fork repository from avengers main to orgnization superheroes-munnep
- branch the new fork repostiry to a feature-release using git-cli
- make changes to the README.md
- create a merge to the avengers main repository 
- delete the branch feature-release

## steps
1. login to your github account account  
[https://github.com/](https://github.com/)
2. Go to the repository munnep/avengers main branch
![](media/2021-10-13-13-59-45.png)  
3. On the top right side click on **Fork**
![](media/2021-10-13-14-00-24.png)  
4. Select **superheroes-munnep**  
![](media/2021-10-13-14-00-58.png)  
5. Now we have a new repository called **superheroes-munnep/avengers**
![](media/2021-10-13-14-02-07.png)  
6. We need to create a new branch called feature-release
Click on **main** -> Switch branch -> **feature-release** -> click Create branch - feature-release
![](media/2021-10-13-14-05-41.png)  
7. From github get the URL to clone the repository. Click on the Code button to see it
![](media/2021-10-13-14-08-22.png)  
8. Go to your terminal and a directory where you want to clone the git repository to your local machine
9. Clone it with the following command and switch to to feature release
```
git clone https://github.com/superheroes-munnep/avengers.git
cd avengers
git checkout feature-release
```
10. Make some changes to the README.md
11. Just an example
```
[patrick:~/git/avengers] feature-release ± vi README.md 
[patrick:~/git/avengers] feature-release(+2/-0) 32s ± cat README.md 
# avengers
avengers example

We just made this change in the feature release branch

This has been added by a change which was done on a feature-release branch under a fork in a different organization
```
12. Add the files to git for change and commit them locally
```
git add .
git commit -am "made a change exercise 4"
git push
```
*note: If you get an error with git push about your account saying you need a personal access token then take the steps described by [this link](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)*
13. Go back to github and the repository superheroes-munnep/avengers. You should see the change you made under branch feature-release
![](media/2021-10-13-14-28-51.png)  
14. Merge superheroes-munnep/avengers branch feature-release to the repository avengers branch main 
15. klik on pull requests
![](media/2021-10-13-14-32-27.png)  
16. click **new pull request**  
![](media/2021-10-13-14-33-19.png)  
17. Check that you merge the branch feature release from superheroes-munnep/avengers to munnep/avengers  
![](media/2021-10-13-14-34-55.png)  
18. click the **Create pull request**
![](media/2021-10-13-14-34-55.png)  
19. give it a correct name and description and click **create pull request**
![](media/2021-10-13-14-36-37.png)  
20. Click the **Merge pull request** 
![](media/2021-10-13-14-37-55.png)  
21. Click **Confirm Merge**
![](media/2021-10-13-14-38-27.png)  
22. Click **delete branch**  
![](media/2021-10-13-14-38-59.png)  
23. You should now see your changes on the main branch of the munnep/avengers repository
![](media/2021-10-13-14-40-01.png)  