WIP: at current state bot has not been tested after pushing it to github and there is no package file for npm packages to install. If you wanna try it out you have to do some configuring. I'll be testing and setting up this as I go that it work later on. Code in itself should work, but at this state it hasn't been tested to work.

# Telegrambot
Telegrambot with daily messages and commands to get information, like train-timetable, weather, and news. It also enables making simple reminders. Also it supports voice messages in english language. Voice message is sent to Microsoft Watson voice-recoqnition API and it tries to detect what you said.

example command can be found by typing in chat where the bot is running by /help

## example images

(Timestamps in these telegram photos are in different time zone, than the actual bot.)

reminders

![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip1.PNG)
![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip6.PNG)

VR train timetable from point A to point B.

![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip3.PNG)

weather data

![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip4.PNG)

heads or tails

![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip5.PNG)

random gif or semi-random with tag.

![alt tag](https://github.com/Crare/telegrambot/blob/master/example_images/snip7.PNG)


# Setting up
* Set all api keys that are needed in the "settings_template.json".
* Add also your bot token keys for testing bot and production, can be same if you don't mind same bot being in production.
* Rename "settings_template".json as "settings.json".

## run bot by:
    node bot_commands.js
  
  or test bot by:
  
    node bot_commands.js --test

## cronjob for daily messages:
  You could use forever.js for running node in the background.
  command example:
    forever start bot_cronjob.js --cronjob --MorningMessage
    
  or test bot:
  
    forever start bot_cronjob.js --test --MorningMessage
    
 All the possible arguments can be seen in bot_cronjob.js at cmdargs. I'll at them here as a list later on.
