# MDAnalysis Bot

This repo contains the source code for the MDAnalysis' Discord bot.
The bot is a fork from the [OBS Support Bot](https://github.com/obsproject/obs-bot)

While the bot is open source, batteries are not included, and there is 
**no support** for third party users. Please do not open issues for such use cases.

## Setup

1. Setup PostgreSQL server version 10+
2. Create database with schema provided in `data/db_schema.sql`
3. Create a Github webhook. See below
4. Setup a webserver passing the hooks. Example nginx configurations in `data/nginx.example.conf`
5. Install Python 3.8+ and dependencies in `requirements.txt`
6. Create configuration file (example in `data/config.example.toml`)
7. Run `python3.8 runner.py -c path/to/your/config-file.toml`
8. ???
9. Profit!

## Webhooks

Create the webhook for your Github project and use the following settings

* Payload URL: `https://my.server.com/github`
* Secret: leave empty
* Content type: `application/json`
* SSL verification: Enable SSL verification 
  (depending on your webserver)
* Let me select individual events: Issues, Pull requests

## Webhooks

Create the webhooks for your github project.

* Payload URL: `https://my.server.com/github`
* Secret: leave empty
* Content type: `application/json`
* SSL verification: Enable SSL verification 
  (depending on your webserver)
* Let me select individual events: Issues, Pull requests


## License

The MDAnalysis Bot source code is licensed under the GNU General Public License v3.
