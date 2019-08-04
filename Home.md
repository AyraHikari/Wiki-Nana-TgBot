# Welcome to the Nana Userbot & Assistant wiki!
All user guide and documentation is here!

Seeking extra help? Don't be shy, come join and ask our [Community](https://t.me/AyraSupport)!
***

## Requirements

- Python 3.4 or higher.
- [A Telegram API key](https://my.telegram.org/apps).
- PostgreSQL Server. (optional)

```
For windows user, please use Python 3.6.7 release or Newest instead!
```

***
## Create a Real Bot

1. Go to @BotFather, then type `/newbot`
2. Insert your bot **Name**, for example **My Assistant**
3. Then insert your bot **username** It must end in `bot`. for example **MyAssistantBot**.
4. Copy Token for later

***

## Configuration

1. Register your account API [here](https://my.telegram.org/apps)
2. Copy api_id and api_hash for config later.
3. Go to [@EmiliaHikariBot](https://t.me/EmiliaHikariBot) or [@MissRose_bot](https://t.me/MissRose_bot), and type `/id`. Copy your ID account.
4. Rename **config.example.py** to **confing.py** in nana folder
5. And change config like this:

```
api_id = 12345 # From guide no 2
api_hash = "123456789abcdefghijklmnopqrstuvw" # From guide no 2
DB_URL = "postgres://username:password@localhost:5432/database" # Create database later

ASSISTANT_BOT_TOKEN = "TOKEN" # Replace TOKEN from guide above (@BotFather)

Owner = 388576209 # From guide no 3
AdminSettings = [388576209] # From guide no 3
```

***

## Install Requirements
Before install python requirements, you need to install some dependencies for prevent got error

***

### Linux user
> Install postgresql first for prevent failing build in pip
```
sudo apt-get update && sudo apt-get install postgresql
```

***

### Android (Termux) user
> You need to perform update and install all dependencies for prevent failing build some pip requirements
```
pkg update && pkg install clang git postgresql python libcrypt-dev libjpeg-turbo
```

***

## Install Python Requirements
Install all requirements python, in your terminal type this
```
pip install -r requirements.txt
```

If you're using pipenv, use this instead
```
pipenv install -r requirements.txt
```

***
## Install Database
This is required for some features, if you want to use database, follow this guide.

***

### Linux user
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

***

### Windows user
You can download Postgresql server [here](https://www.postgresql.org/download/windows/)

***

### Android (Termux) user
- Install postgresql (if not installed)
```
pkg update && pkg install postgresql
```

- After installing postgres, run server with this
```
initdb ~/pg
pg_ctl -D ~/pg start
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

***

## Run NanaBot and Assistant

To run this bot, just type
```
python -m nana
```

Or if you're using pipenv, do this instead
```
pipenv run python -m nana
```

***

# Getting update

Assistant will check update every bot is running, make sure you're on official branch.

To check update manual, just type `update` with Command (default is .) in your nana bot.
To get update, type `update now` in your nana bot.

> Or you can update via Assistant (If they notify you), just click Update Now and wait for update!

Seeking extra help? Don't be shy, come join and ask our [Community](https://t.me/AyraSupport)!

***

# Contributing

Nana userbot is brand new, and you are welcome to try it and help make it even better by either submitting pull requests or reporting issues/bugs as well as suggesting best practices, ideas, enhancements on both code and documentation. Any help is appreciated!

***
