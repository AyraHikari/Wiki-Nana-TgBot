## Install Termux
Termux is an Android terminal emulator and Linux environment app that works directly with no rooting or setup required.

To run python you need this app
> https://play.google.com/store/apps/details?id=com.termux

Also you can install kali nethunter in your android, but that was for **advanced user only**.

> Before you go next guide, please look [this note first](https://github.com/AyraHikari/Nana-TgBot/wiki/Install-on-Android#note), so if something is wrong, you will know what to do next!

## Install Termux Requirements
You need this to run your bot
```
pkg update && pkg install clang git postgresql python libcrypt-dev libjpeg-turbo
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
pip install -r requirements.txt
```

If you're using pipenv, use this instead
```
pipenv install -r requirements.txt
```

> Install database is optional, if you want to use database in your bot, then follow this guide

## Install database
You need to install postgresql first for prevent failing build when installing python requirements
```
pkg update && pkg install postgresql
```

## Create a database
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

## Note

Please note, in some devices will have failing install on requirements.

If you facing that problem, please come join and ask on our [Community](https://t.me/AyraSupport)!