# Cinema API

This is application for managing cinema, written in Django REST framework (DRF). 
It provides endpoints for managing movies, cinema halls, orders and tickets, as well as user authentication and authorization. 

## Futures:
- Creating movies with description and picture
- Creating genres, actors, cinema halls
- Creating tickets and orders 
- Managing tickets and orders 
- Adding movie sessions
- Filtering movies and movie sessions
- Authenticate with JWT
- Admin panel /admin/
- Documentation is located at /api/doc/swagger/


### Instaling usig GitHub:
Install PostgreSQL and create db
```
git clone https://github.com/inrock1/Cinema-API.git 
cd cinema_API 
python -m venv venv 
source venv/bin/activate (for Mac OS)
venv\Scripts\activate (for Windows)
pip install —r requirements.txt
rename file .env.sample in .env and put your DB credentials

python manage.py migrate 
python manage.py runserver
```
### Run with docker
Docker should be installed
```
docker-compose build
docker-compose up
```

### To get access to the app
- Go to registration page and enter email with password to use for access  
http://127.0.0.1:8000/api/user/register/
- After registration proceed to token page. Enter email and password to obtain access token. Save it to use later  
http://127.0.0.1:8000/api/user/token/
- Now you are ready to proceed with using service by submitting access token in http request header. 
You can use ModHeader plugin for your browser. 
- start from this endpoint:  
   http://127.0.0.1:8000/api/cinema/  
   http://127.0.0.1:8000/api/doc/swagger/
