# Django Polls Sample App 

Django makes it easier to build better Web apps more quickly and with less code.[Get started with Django](https://www.djangoproject.com/start/)

This application is a sample Django polls application using Postgres database 
 
## Set up on Azure
* Create a Postgres server and database on Azure . Many options are available for postgres as listed [here](https://azure.microsoft.com/en-us/search/marketplace/?q=postgres).
* Import the database schema in the [djangopollschema.sql](https://github.com/SunBuild/djangopollapp/blob/master/djangopollschema.sql)
* Click on [![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)
* Add AppSettings (key/value pair) for your web app 
```
DATABASENAME = <your-db-name>
DATABASEUSER = <your-db-user>
DATABASEPASSWORD = <your-db-password>
DATABASEHOST= <your-db-host>
```  
* Open the KUDU debug console for your web app ( URL format is https://sitename.scm.azurewebsites.net).Run the following DJANGO migrate command to sync the models in this app with your database. 

```
D:\home>CD d:\home\site\wwwroot
D:\home\site\wwwroot>env\Scripts\python.exe manage.py migrate 
```

* Browse the site . You can access the django administration site with these credentials 
```
User: djadmin
Password: superuser 
```

 

