## Install Linux Requirements
You need this to run your bot
```
apt update -y && apt install git postgresql python3 python3-pip  python-psycopg2 libpq-dev -y
```

## Clone repository
Don't forget to clone repository, do this
```
git clone https://github.com/AyraHikari/Nana-TgBot
```
And then change dir to that repo
```
cd Nana-TgBot
```

## Install Python Requirements
Install all requirements python, in your terminal type this
```
pip3 install -r requirements.txt
```

If you're using pipenv, use this instead
```
pipenv install -r requirements.txt
```

> Install database is optional, if you want to use database in your bot, then follow this guide

## Install database
You need to install postgresql first for prevent failing build when installing python requirements
```
sudo apt-get update && sudo apt-get install postgresql
```

## Create a database
- Install postgresql (if not installed)
```
sudo apt-get update && sudo apt-get install postgresql
```

- Change user to postgres
```
sudo su - postgres
```

- Create a user, change **YOUR_USER** with you own user
```
createuser -P -s -e YOUR_USER
```

- Create a database, dont forget to change **YOUR_USER** and **YOUR_DB_NAME**
```
createdb -O YOUR_USER YOUR_DB_NAME
```

- Test your database (optional)
```
psql YOUR_DB_NAME -h YOUR_HOST YOUR_USER
```

- After create a database, your database URL should be like this
```
postgres://YOUR_USER:password@localhost:5432/YOUR_DB_NAME
```