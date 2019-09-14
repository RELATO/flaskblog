# Flask Blog python3 demo app

## Installing python3 just in case
[Install Python3 on mac](https://wsvincent.com/install-python3-mac/)

## Clone the repository 
```
cd ~ 
git clone https://github.com/RELATO/flaskblog.git
cd flaskblog
```

## Installing the dependencies
```
pip3 install -r requirements.txt
```

## Developing on macos and mysql client
You need to run the command below to install mysqlclient
```
env LDFLAGS="-I/usr/local/opt/openssl/include -L/usr/local/opt/openssl/lib" pip3 install mysqlclient
```

and after run
```
pip3 install configparser
pip3 install mysql-python
``` 

## Generating the SECRET_KEY
```
python3
>>> import secrets
>>> print("Generate a secure hexadecimal token", secrets.token_hex(32))
``` 
You should see a message like the this
```
Generate a secure hexadecimal token 7865b88579dd1f82b36ec479b9b269c63c59a0a166f3f293c9ddb93b1f08ccc6
```

## Creating the mysql database

In your mysql use the command below to create database 
```
CREATE DATABASE flaskblog;
```

Replace the statement below with your [dbuser] and [userpassword] before executing it
```
export SQLALCHEMY_DATABASE_URI='mysql+mysqldb://[dbuser]:[userpassword]@localhost/flaskblog'

python3 dbcreate.py
```


## Running the app
Replace the statement below with your [dbuser] and [userpassword] before executing it
```
export SQLALCHEMY_DATABASE_URI='mysql+mysqldb://[dbuser]:[userpassword]@localhost/flaskblog'

export SECRET_KEY=7865b88579dd1f82b36ec479b9b269c63c59a0a166f3f293c9ddb93b1f08ccc6


python3 run.py
```

## Credits and references

[Tutorial](https://www.youtube.com/watch?v=MwZwr5Tvyxo&list=PL-osiE80TeTs4UjLw5MM6OjgkjFeUxCYH)

