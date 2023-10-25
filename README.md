# TechStore

### These are the steps i took to create this project
### You are welcome to use this project as you please

1. Open Git hub and then open repositories then click the green create button on the top right then by repositories name, name your project then scroll down and click create repository

2. Then click the open in gitpod green button

### In git pod *****

3. When gitpod open type this in your terminal: pip3 install 'django<4'

4. Then type this in your terminal: pip3 install django-allauth==0.41.0

5. Then type this in your terminal: django-admin startproject YOUR PROJECT NAME .

6. Create a basic gitignore file by typing: touch .gitignore then in gitignore file add these: *.sqlite3 *.pyc __pycache__

7. Then type this in your terminal: python3 manage.py runserver

#### Your project should open in ther browers showing this: DisallowedHost at / Invalid HTTP_HOST header copy and paste this link into your settings.py allowed host: '8000-donnavanstadd-techstore-5hxkhqpe0wb.ws-eu105.gitpod.io'
 
Inline-style: 
![alt text](allowed_hosts.jpeg "Logo Title Text 1")

8. Stop server by pressing ctrl and c at the same time

9. The run initial migrations by typing this in your terminal: python3 manage.py migrate

10. Create superuser to login to admin by typing this in terminal: python3 manage.py createsuperuser

11. Then create a username the hit enter, then enter email then hit enter, then password

12. Now push your work to github by clicking the plus button next to changes just under the orange button on the top left called commit, then type initial commit in the message box above the orange commit button, then click the orange commit drop down, then click commit and push, you have now pushed your project to github congrates.

### Registartion
13. In terminal type: pip3 install django-allauth==0.41.0

14. [Follow this link to allauth.org](https://docs.allauth.org/en/latest/installation/quickstart.html)

15. copy this from allauth.org and paste it in settings.py: 
#### AUTHENTICATION_BACKENDS = [
 ####  'django.contrib.auth.backends.ModelBackend',

  #### 'allauth.account.auth_backends.AuthenticationBackend',
]

16. copy and paste this in settings.py/ INSTALLED APPS

    #### 'django.contrib.sites',
    #### 'allauth',
    #### 'allauth.account',
    #### 'allauth.socialaccount',

17. In settings.py add this below AUTHENTICATION_BACKENDS: SITE_ID = 1

18. Paste this in urls.py/urlpatterns: path('acounts/', include('allauth.urls')), also add include at the top by imports

19. Then run migrations to update the database by typing this in teminal: python3 manage.py migrate 

20. Then run server: python3 manage.py runserver
21.Navigate to admin: by adding /admin after your url: https://8000-donnavanstadd-techstore-eob2xdfff9e.ws-eu105.gitpod.io/admin/login/?next=/admin/
22. login, if you cannot login create a superuser
23. when logged in click on sites and update the domain of the default site its called example.com click on it to yourwebsitename.example.com and change dispaly name to your website name like Tech Store is mine then click save

24. this is for log in copy and paste this in your settings.py under SITE_ID:

#### EMAIL_BACKEND = 'django.core.mail.backends.console.EmailBackend'

#### ACCOUNT_AUTHENTICATION_METHOD = 'username_email'
#### ACCOUNT_EMAIL_REQUIRED = True
#### ACCOUNT_EMAIL_VERIFICATION = 'mandatory'
#### ACCOUNT_SIGNUP_EMAIL_ENTER_TWICE = True
#### ACCOUNT_USERNAME_MIN_LENGTH = 4
#### LOGIN_URL = '/accounts/login/'
#### LOGIN_REDIRECT_URL = '/success'

25. test it by running the server navigate to /accounts/login, if it just says success you need to log out of admin by going to /admin and log out the try again by going to /accounts/login if you login and it say Verify Your E-mail Address
We have sent an e-mail to you for verification. Follow the link provided to finalize the signup process. Please contact us if you do not receive it within a few minutes. you succefully created a login page

26.Push to git hub