# my_first_api
Advanced API with good syntax 

# steps to upload larger files
git remote add origin https://qifengzhou.github.io/2018/04/29/Upload%20files%20bigger%20than%2025%20MB%20to%20Github/

#  click on the request


# advanced error handle

#### this help you to send mails when alot of errors happends
https://flask.palletsprojects.com/en/1.1.x/errorhandling/


# email with flask (easy from localhost)

1. turn off this feature becuase localhost not useed SSL it act like bad app () Turn it off after finish emails 
*  https://myaccount.google.com/lesssecureapps  (turn on mail from localhost will work)

*  if you have SSL add this ```app.config['MAIL_USE_SSL'] = True```

2. config

```
pip install flask-mail 
from flask_mail import Mail, Message

    app.config['MAIL_SERVER'] = 'smtp.googlemail.com'
    app.config['MAIL_PORT'] = 587
    app.config['MAIL_USE_TLS'] = True
    app.config['MAIL_USERNAME'] = '******'
    app.config['MAIL_PASSWORD'] = '******'
    mail = Mail(app)
    
    to sent email to one or list of users
    msg = Message('Hello World My First Mail', sender = 'yourmailid@gmail.com', recipients = ['reciver_mail@gmail.com'])
    msg.body = "Your message"
    mail.send(msg)

```
