using guidance from:
http://www.marinamele.com/2014/02/how-to-install-celery-on-django-and.html  
required: celery, django-celery  
djcelery imports django-celery and this used the django database(probly not such a good idea)  

python manage.py makemigrations  
python manage.py migrate  

pip freeze > requirements.txt saves currevtn env reqs.  

python manage.py celeryd --verbosity=2 --loglevel=DEBUG  
python manage.py celerybeat --verbosity=2 --loglevel=DEBUG  

had to correct BROKER_URL  
had to add pickle to CELERY_ACCEPT_CONTENT  

rabbitmqmgmt @ http://localhost:15672/#/ 

... didn't learn much from this as it doesn't have a view, celeryd tasks seem to show up in rabmq though 
