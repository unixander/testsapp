# Tests App

## Admin dashboard

### Users

* Users - lsit of registered users
* User's Topic Results - allows to view users answers by topics
* User answers - list of answers by user and question

### Questions

* Questions - list of questions, that allows to add answers
* Topics - list of topics, allows to make groups of questions by topics


## Install

### For local deployment

* Run ```pip install -r requirements.txt```
* Create .env file in root folder. Example of variables is in example.env file.
* Create settings_local.py in root folder and redefine settings for local ones.
* Run ```./manage.py migrate```
* Run ```./manage.py loaddata sample_data.json``` to load sample data to database
* If you ran previous step then now you have 2 users: admin and moderator
* admin - (login/password: admin/123admin789) superuser with access to all sections of admin panel
* moderator - (login/password: moderator/123test789) user with access to admin dashboard, but with restrictions for sections access
* Run ```./manage runserver``` to run server locally

### Running tests

* Run ```pip install -r requirements/test.txt```
* Create .env file in root folder. Example of variables is in example.env file.
* Create settings_local.py in root folder and redefine settings for local ones.
* Run ```./manage test --settings=settings_test```
