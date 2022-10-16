# django_email_celery

This project sending emails using Celery.

## requirements.txt
```
amqp==5.1.1
asgiref==3.5.2
async-timeout==4.0.2
billiard==3.6.4.0
celery==5.2.7
click==8.1.3
click-didyoumean==0.3.0
click-plugins==1.1.1
click-repl==0.2.0
colorama==0.4.5
Deprecated==1.2.13
Django==4.0.8
django-celery-beat==2.3.0
django-celery-results==2.4.0
django-timezone-field==5.0
kombu==5.2.4
packaging==21.3
prompt-toolkit==3.0.31
pyparsing==3.0.9
python-crontab==2.6.0
python-dateutil==2.8.2
pytz==2022.4
redis==4.3.4
six==1.16.0
sqlparse==0.4.3
tzdata==2022.5
vine==5.0.0
wcwidth==0.2.5
wrapt==1.14.1
```


## Setup Repo
virtualenv -p python3 /.<br>
source bin/activate<br>
git clone https://github.com/ozbeysait/django_email_celery<br>
cd django_email_celery<br>
pip install -r requirements.txt<br>


## Set Your Settings
Set your Django Secret Key and SMTP settings<br>
![image](https://user-images.githubusercontent.com/41578459/196013784-7b1b31f0-844b-4b14-bbf9-cd21a5789c98.png)


## Runserver
```
python manage.py makemigrations
python manage.py migrate 
python manage.py runserver
```
![image](https://user-images.githubusercontent.com/41578459/196013877-635f1cd6-9570-4d07-b83d-2f5281f0bae2.png)


## Run Celery
```
celery -A django_email_celery.celery worker --pool=solo -l info
```
![image](https://user-images.githubusercontent.com/41578459/196013909-36958a3b-fd24-4f4f-82e7-e5f0d2c5f6e4.png)


## Send email from an endpoint
Go to the http://127.0.0.1:8000/sendmail/<br>
![image](https://user-images.githubusercontent.com/41578459/196013941-641d7b73-6f69-4508-ae1a-d5ef78a7dadb.png)

### Check Celery
![image](https://user-images.githubusercontent.com/41578459/196013959-34f1b0ff-49c2-406f-85e0-51d74a36c891.png)

## Result
![image](https://user-images.githubusercontent.com/41578459/196013969-08259b06-c181-4210-9677-50e96e649864.png)







