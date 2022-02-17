# Milestone 3 - App development an deployment in R

This week you will setup a new project on GitHub.com, and recreate your dashboard using the R implementation of dash and plotly.
You will see in lecture that the app skeleton and the entire layout part is very similar to what you have done in Python.
You will also respond to you TAs feedback for milestone 1, and explore if you can implement any of their suggestions, details below.
You will also give feedback to another group on their dashboard.

## 1. Submission instructions

- We need a public github.com repo for deployment. This will also make it easy to share a link to your work as part of your portfolio. You will get a new template repo for your R dashboard, name your repo something memorable, keep the name the same as Milestone 1 & 2, but just add R.
- Use the same repo for Milestone 3 and 4 for your R Dashboard.
- Pick a suitable licence. MIT and BSD-3 are common good options for open source projects. [The carpentries has a short primer on licenses](http://swcarpentry.github.io/git-novice/11-licensing/index.html) (optional read).
- You will submit your repos on Gradescope, as usual.

### Create a new github.com repo for your dashr project (Accept a new GH Classroom link)

- You will create a new repo for this project
- Name it the same as your Python dashboard repo plus a `-R` suffix so it is easy to find.
    - `your-previous-repo-name-R`
- Copy over your contributing guidelines, code of conduct, teamwork contract, README file, and any data files.
    - Update your README with a link to the deployed R dashboard and a new image/gif of the R dashboard in action.

### Tips for working collaboratively on GitHub

- Every time you work on the project, you should first pull the upstream changes.
- Use GitHub issues to track features that you are planning to implement
  and bugs in the app.
- Try to commit to git often when you work on this project.
    - If you are working together synchronously
      and a team-member has already approved your changes,
      you can commit directly to the main branch.
      Otherwise, create a pull-request and request a review from a teammate.
        - **The TAs will check that you have some issues and PRs in your repo for this milestone**
    - You can either work on different branches directly in the repo you created,
      or fork the repo and work on a branch in your own fork.

## 2. Deployment on Heroku

**There may be some issues with dash-R deployment because plotly recently updated their docker images, but not their documentation.
Budget extra time for the R deployment!**

- Deploy your app on Heroku and **include the link to your deployed dashboard clearly visible near the top of your README**.
- Don't push to Heroku after the milestone deadline.
- Heroku does not have native support for R so we will need to use a docker image provided by Dash.
    - We will [follow the dash docs](https://dashr.plotly.com/deployment).
        - You need to change the `Dockerfile` to make sure you get version `3.6.3` or higher.
        - Conveniently, as of February 2022, the DashR deployment page is not quite available.
    - Because of this, I don't want to change the file structure from the docs, so put your `app.R` in the root project folder (together with all other files mentioned in the deployment docs),
    - Any other folders can be the same as for your Python project.
- Don't wait to deploy until the last minute, you will not have time to solve potential issues.
    - Deploy early and check that things are working, then redeploy every now and then.
    - After making the milestone release, make a final push to Heroku to redeploy the milestone app.
    - This is especially important for R, since it takes about 15 min for the docker image to deploy.

## 3. Interactive Dash app with R and ggplotly

- Implement the same dashboard as in milestone 2.
- **You don't need to rewrangle your raw data**
    - I you already have processed data files, feel free to use those.
- The goal is to implement most of your milestone 2 dashboard so that you can compare dashboard development in Python and R.
    - Your should be able to get your app layout to look very similar as milestone 2.
    - For the plots, there might be parts that are not possible to implement the same as in Altair without a lot of work and those you can skip or design differently. There might also be parts that are easier to implement with ggplotly, so it makes sense to design it in another way.
- The main reason to deviate from your milestone 2 dashboard is if your TA has given you feedback that you want to implement. For milestone 3 you are expected to reply to you TAs feedback on your proposal from milestone 1.
    - For aspects of the feedback that you plan on implementing, create new issues and link to the issue your TA created so that they can easily find the new ones.
    - For aspects that you want to keep discussing with your TA, you can reply to them in the issue they created or chat with them during lab or OH.
        - If you do the latter, please document briefly in the issue what you agreed to in person.
    - When grading this milestone, your TA will check the miestone 1 feedback issue they created for comments and links to features you plan to implement, so make sure to include these!

- **It is up to you whether you want to implement the TA feedback in this or the next milestone.**
    - I know quiz weeks are tough, so I will let you plan your own time for this task.
    - For milestone 4, you will need to have replied to all your TA feedback from milestone 1 and 2, and have implemented some suggested features.
        - So if you want to focus on the quizzes this week and implement most of the feedback next week that is totally fine (you still need to reply to the feedback from milestone 1 and create issues for what you plan to implement as described above).
    - For milestone 4, you will choose to work in either R or Python, so your strategy for milestone 3 could be to either develop exactly the same app to compare with last week, or since your are starting over anyways, try to implement some TA feedback and see how you like it compare to your original design.
- Again, the app should be easily usable, so focus on the most important things first.
- Note that TAs will be grading your app on Heroku in a full-screen window
- **Do not get hung up of minor styling details, you will get to this in milestone 4!**

## 4. Reflection

In this section, your group should document on what you have implemented in your dashboard so far and explain what is not yet implemented.
It is important that you include what you know is not working in your dashboard, so that your TAs can distinguish between features in development and bugs.

This week it is suitable to include some brief thoughts on the experience of implementing the dashboard a second time in another language.
You could also mention some feedback you have received and how that has impacted your future planning.
This section should be around 300-400 words and the `reflection-milestone3.md` document should live in your GitHub.com repo in the `doc` folder.