## Update via Bot
Assistant will check update every bot is running, make sure you're on official branch.

> If you're hosted in Heroku, git dir will be deleted in your app, you can do `update now` to repair that!

* To check update manual, just type `update` with Command (default is .) in your nana bot.
* To get update, type `update now` in your nana bot.
* You can update via Assistant (If they notify you), just click Update Now and wait for update!

## Update manual
You can update manual, if you're on your forked git, just follow this guide

* Create remote upstream
If you already have that remote, go next!
```
git remote add upstream https://github.com/AyraHikari/Nana-TgBot
```

* Fetch update from upstream
```
git fetch upstream
```

* Update from upstream
If you're on other branch, **change master** branch to **your current branch**
```
git pull upstream master
```

**Got an error?**

If you have modified files, you can backup that files before revert that!
```
git checkout *
```
Or reset all
```
git reset --hard
```
Then you can pull again


> Note: Sometimes soft reboot doesn't take any changes, just restart your bot manual to take any changes.

***

Seeking extra help? Don't be shy, come join and ask our [Community](https://t.me/AyraSupport)!