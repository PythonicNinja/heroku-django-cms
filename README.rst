Fully working step by step project to deploy Django 1.5.1 + Django-cms 2.4.2 on Heroku

1. Clone git repo from github, requires git client.

    $ git clone git://github.com/YoungCoder/heroku-django-cms.git
    
2. Go into the new project directory
    
    $ cd django-cms-heroku

3. Create the virtualenv (if you don't have pip install virtualenv)

    $ virtualenv --no-site-packages --distribute django-cms-heroku

4. Sign-Up for a Heroku account. https://api.heroku.com/signup

5. Install the Heroku client. http://devcenter.heroku.com/articles/quickstart

6. The first time you use the Heroku client you will need to login using the same information you used when you signed up. Follow the prompts, and it will finish your install.

    $ heroku login

7. Create your heroku application

    $ heroku create --stack cedar

8. Push your code into heroku

     $ git push heroku master

9. Sync your database and create your admin account.

     $ heroku run python mycms/manage.py syncdb

10. Run your database migrations.
    
     $ heroku run python mycms/manage.py migrate

13. Open application in your browser and start using djangoCMS on heroku.

     $ heroku open


09 07 2013 - Poland
YoungCoder - vojtek.nowak@gmail.com

Once you get comfortable with how things work, you could add more plug-ins, create your own custom templates and then change your DEBUG setting to False.
After you make changes to your local project directory, you can test it on the server by running the git push command again.

For more info about Heroku and django-cms and what you can do with with it. check out their docs
 - http://devcenter.heroku.com/categories/platform-basics
 - https://www.django-cms.org/en/documentation/

Links:
 - **Virtualenv** : http://pypi.python.org/pypi/virtualenv
 - **pip** : http://www.pip-installer.org/
 - **virtualenvwrapper** : http://www.doughellmann.com/projects/virtualenvwrapper/
 - **git** : http://git-scm.com/
 - **orginal poster for django 1.3 ** https://github.com/kencochrane
 
