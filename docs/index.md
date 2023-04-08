# Setting up Aperture

## Adding and setting up Aperture
Firstly, add Aperture to your server by using this link: https://add.aperturebot.science/. There are no requirements to add Aperture to your server. Once the bot has been added to your server, type the following in any text channel (on your server): `@Aperture#8658 setup`. This will add you to your servers config on the dashboard.

Once Aperture has been setup, go to https://dashboard.aperturebot.science to edit your server's configuration. Use the sidebar to read about each plugin, then use the example below along with the information in the sidebar to set up your own customized Aperture configuration.

Below is a blank configuration example with web, utilities, admin, infractions, modlog, spam, and censor set up. 

**Do not copy this example. Do not copy the examples in the plugins.** 

These are meant to guide you in creating your own config. Copying them will result in unexpected functionality, and may open your guild to unexpected security flaws.

```yaml
web:
  000000000000000000: admin  #Username
  000000000000000000: editor #Username
  000000000000000000: viewer #Username

commands:
  prefix: '!'
  overrides: []

levels:
  000000000000000000: 000 # Role
  000000000000000000: 000 # Role
  000000000000000000: 000 # Role

nickname: Aperture

plugins:

  utilities:
    auto_role: [000000000000000000]

  admin: {}

  tags: {}

  infractions:
    mute_role: 000000000000000000
    notify_actions: [WARN]
    show_moderator: false
    silence_level: 100

  modlog:
    channels:
      000000000000000000:
        exclude: []
        include: []
    ignored_users: []

  censor:
    levels:
      0:
        filter_invites: true
        invites_whitelist: ['discord-developers', 'discord-testers', 'discord-api', 'events', 'discord-linux', 'gamenight', 'discord-feedback']
        blocked_words: ['word1', 'word2', 'word3']
#     channels:
#      000000000000000000:
#        blocked_words: ['word4']
```
