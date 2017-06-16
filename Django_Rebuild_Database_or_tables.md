# Django 1.11 Rebuild Database or Tables
Sometimes database of some tables should be deleted, but an error "Tabel ** doesn't exist!" may happen.
To solve the problem, I have do the following steps:
1. Backup all code;
2. delete all files except models, apps and urls in the app;
3. Comment out the content of urls
4. Run "python manage.py makemigrations", and make sure there is not the error;
5. Run "python manage.py migrate" without the error
6. Restore all files of the app.