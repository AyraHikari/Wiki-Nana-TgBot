# Requirements

- Have official bot token.
- You have session file for your account. (login pyrogram)
- A brain

# Create an App

1. Make sure you're logged in on Heroku, if not [login here](https://dashboard.heroku.com/login)
2. [Go here](https://dashboard.heroku.com/new-app) to create a new app, then fill form as you like
3. After created a new app, follow setup wizard until done.
4. [Go here](https://dashboard.heroku.com/apps), and select your app
5. Then you're ready to go next guide

# Use Heroku CLI
- You can download and install Heroku CLI in here
> https://devcenter.heroku.com/articles/heroku-cli

- Open CMD/Terminal, And login to your heroku account
`heroku login`

- Clone your app
`heroku git:clone -a your-app-name`

- Change dir to workdir
`cd your-app-name`

- Clone repository
**You need to install git command**, google it if you dont know how to install that!
```
git remote add upstream https://github.com/AyraHikari/Nana-TgBot
git pull upstream master
```

- Create a PostgreSQL
1. [Go here](https://dashboard.heroku.com/apps), and select your app
2. Go resources tab, then search `Heroku Postgresql` in Add-ons, click that, and select Hobby Dev
3. You've created a postgresql, open that and then new tab will open
4. Go to Settings tab, View Credentials, copy URI for config later

- Configuration
1. [Go here](https://github.com/AyraHikari/Nana-TgBot/wiki/Configuration) and come back to here after you're create a config.py!
2. Create a file name `Procfile` and fill this:
```
worker: python3 -m nana
```

- Push to heroku
```
git add .
git commit -am "Initial commit"
git push heroku master
```

- Start bot
```
heroku ps:scale worker=1
```

- Stop bot
```
heroku ps:scale worker=0
```

- Get log
```
heroku logs --tail -a your-app-name
```

- Restart bot
```
heroku ps:restart
```