# Python-gunicorn-Heroku
Deploying python app on Heroku using gunicorn

Heroku has a free service model for small projects.It is a Platform as a Service that sits on top of AWS to provide an experience that is specifically designed to help developers to deploy,manage and scale their apps written in Ruby, Node.js, Java, Python, Clojure, Scala, Go & PHP.

If you want your application running on Heroku , you will have to know some commands on Heroku CLI & Dashboard.

The Heroku Command Line Interface (CLI) makes it easy to create and manage your Heroku apps directly from the terminal.
----------------------------------------------------------------------------------------------------------------------


The Heroku Dashboard is the primary web interface for interacting with the Heroku platform. It provides UI support for tasks like:

Creating Apps

Renaming Apps

Deleting Apps


 Prerequisites:
 ---------------
 

Git Installed on system

Sign up for a Heroku account

Install heroku CLI using:
                 
                 $ sudo snap install --classic heroku



 
Step # 01:
---------

 - Clone the Project from Github.

Ref: https://github.com/Cryptic-Gemini/Python-gunicorn-Heroku.git
 
Normally, Flask run in single-threaded mode, and can only handle one request at a time, and any parallel requests should wait until they can be handled. You can solve this problem by putting threaded=True in app.run.
 
                app.run(port=2020, threaded=True)
 
Step # 02:
--------------

 - Create a Procfile 
 
           web: gunicorn app:app

The web command tells Heroku to start a web server for the application, using gunicorn. Since our application is called app.py, we've set the app name to be app as well.

Step # 03:
-----------

- After you install the CLI, run the heroku login command. You’ll be prompted to enter any key to go to your web browser to complete login. The CLI will then log you in automatically.

                 $ heroku login

 
 
Step # 04:
-------------

- Initialize a local Git repository and commit your application code to it.

Note: You should initialize the Git repository in the app’s root directory.Otherwise it will not run when deployed on Heroku.

                $ cd python-heroku-gunicorn

                $ git init
 
                $ git add .

                $ git commit -m “My first commit”

Step # 05:
---------

- Create a Heroku app:

                $ heroku create app-name

You can give any name of your choice instead of app-name.

For example :

             $ heroku create python-gunicorn-face

When you deploy your application on Heroku,you will have to choose a unique name for your application. 

 
Step # 06:
------------

- Add a remote to your local repository

              $ heroku git:remote -a python-gunicorn-face

 
Step # 07:
------------

- Use the git push command to deploy your app on Heroku

                     $ git push heroku master 
 
 
You will find your app running as:

              https://python-gunicorn-face.herokuapp.com/



 
 
 
 
 











