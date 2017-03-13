#Django Polls Sample App 

[![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://azuredeploy.net/)

Django makes it easier to build better Web apps more quickly and with less code.[Get started with Django](https://www.djangoproject.com/start/)

This application is a sample Django polls application using Postgres database 
 
## Set up on Azure

1. Fork this repo
2. Create an [Azure Web App](http://portal.azure.com) 
3. Create a Postgres server and database on Azure . Many options are available for postgres as listed [here](https://azure.microsoft.com/en-us/search/marketplace/?q=postgres).
4. Import the database schema in the [sample_database.sql]()
5. Add AppSettings (key/value pair) for your web app 
DATABASENAME = <your-db-name>
DATABASEUSER = <your-db-user>
DATABASEPASSWORD = <your-db-password>
DATABASEHOST= <your-db-host>
  
6.Set up GitHub deployment on your web app in the Azure portal
    1. Click on Deployment Options
    2. Choose GitHub
    3. Select the forked repo
    4. Click on Deployment Options again and wait for it to complete
7. Open the KUDU debug console for your web app ( URL format is https://sitename.scm.azurewebsites.net) 
Run the following command

D:\home>CD d:\home\site\wwwroot
D:\home\site\wwwroot>env\Scripts\python.exe manage.py migrate 

8. Browse the site . You can access the django administration site with these credentials 
User: djadmin
Password: superuser 

 

