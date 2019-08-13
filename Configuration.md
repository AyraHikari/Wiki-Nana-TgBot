1. Register your account API [here](https://my.telegram.org/apps)
2. Copy api_id and api_hash for config later.
3. Go to [@EmiliaHikariBot](https://t.me/EmiliaHikariBot) or [@MissRose_bot](https://t.me/MissRose_bot), and type `/id`. Copy your ID account for later.

# Using config file
You can use easily config with config.py file.

1. Rename config.example.py to **confing.py** in nana folder
2. And change config like this:

```
api_id = 12345 # From guide no 2
api_hash = "123456789abcdefghijklmnopqrstuvw" # From guide no 2

ASSISTANT_BOT_TOKEN = "TOKEN" # Replace TOKEN from guide above (@BotFather)

Owner = 388576209 # From guide no 3
AdminSettings = [388576209] # From guide no 3
```

# Using environment variable

## You will need this to generate session string
> https://github.com/AyraHikari/pyrogram-session-maker

How to use session-maker?
Run maker and follow setup wizard: `python maker.py`

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables. The following env variables are supported:

> Star (*) = Means you can fill multiple, separeted by space ( )

### Must be filled
- `ENV`: **You must** fill this for environment work!
- `api_id`: Fill your api_id copied before
- `api_hash`: Fill your api_hash copied before
- `Owner`: From guide no 3
- *`AdminSettings`: From guide no 3
- `USERBOT_SESSION`: [See here](https://github.com/AyraHikari/pyrogram-session-maker) how to generate
- `ASSISTANT_SESSION`: [See here](https://github.com/AyraHikari/pyrogram-session-maker) how to generate

### Optional
- `lang_code`: Language code, `en` for an example
- `device_model`: Device mode, `PC` for an example
- `system_version`: System version, `Linux` for an example
- `ASSISTANT_BOT_TOKEN`: Fill this if you're using session file
- `Command`: Overide command prefix
- `NANA_WORKER`: Overide default userbot worker
- `ASSISTANT_WORKER`: Same like above, but this for assistant
- `REMINDER_UPDATE`: Remind you to update every starting bot, by default is `True`. pass `False` to disable this.
- *`USERBOT_LOAD`: Load module, if module is not filled, don't load that
- *`USERBOT_NOLOAD`: Reverse of above, do not load that module
- *`ASSISTANT_LOAD`: See above
- *`ASSISTANT_NOLOAD`: See above
- `thumbnail_API`: Thumbnail API
- `screenshotlayer_API`: Screenshot API

## Developer only
- `TEST_MODE`: Login to test server
- `TEST_DEVELOP`: Test bot script, if passed then exit bot