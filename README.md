# hello-world-heroku-py
sample project for heroku deployment

Heroku Setup !!!
-----------
* Step 1 - Install the Heroku CLI on your Computer (You can find the procedure here for all OS https://devcenter.heroku.com/articles/heroku-cli)
* Step 2 - Go to Heroku website (heroku.com), login and create a new App; choose a meaningful name for your App.
* Step 3 - Now we need to add a python build path, head over to Settings>Add Build Path>Select the Python Option

Prerequisite for Heroku !!
------------------------
* Before you can deploy an app to Heroku, you need to add two important files which are the Procfile & requirements.txt file
* Procfile Setup

      worker: python YOURSCRIPTNAME.py
* Requirements.txt File Setup


      Create a file (Requirements.txt) inside repo and mention required libraries
  The requirements.txt file makes it easier for Heroku to install the correct versions of the required Python libraries (or “packages”) to run your Python code.

Deploying to Heroku !
--------------------
```
heroku login
heroku git:remote -a <app-name>
git add .
git commit -am "Deployment commit"
git push heroku main 
```

Running the App or bot on Heroku!
---------------------------------

```heroku ps:scale worker=1```

Stop the App on Heroku!
---------------------------------

```heroku ps:scale worker=0```
