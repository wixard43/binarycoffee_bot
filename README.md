# Binary Coffee Bot

**Telegram** bot that publishes the latest articles from our [blog](https://binary-coffee.dev) to our [Telegram channel](https://t.me/binarycoffeedev). If you have a blog with a json1 feed and want to send the posts automatically to a telegram channel you can use this bot.

## Setup project

### Environment variables

* `CHANNEL`: your channel user **@channel**
* `TOKEN`: your bot token, you can see [this post](https://binary-coffee.dev/post/como-hacer-un-bot-de-telegram-desde-cero-con-python)
* `RSS_FEED`: URL of the JSON feed of your blog. example `https://api.binary-coffee.dev/posts/feed/json1`
* `REFRESH_TIME`: interval of time to check for new items. default `60`
* `DATA_ADAPTER`: type of adapter used to save the data. example `MemoryAdapter`|`JsonAdapter`|`MongodbAdapter`
* `DATA_PATH`: (**JsonAdapter**) in case of use JsonAdapter, you can decide where to save the file. default `./data`.
* `DATABASE_HOST`: (**MongodbAdapter**) host for your mongodb database. default `localhost`
* `DATABASE_PORT`: (**MongodbAdapter**) port for your mongodb database. default `27017`
* `DATABASE_NAME`: (**MongodbAdapter**) database name. default `bc_db`

### Steps to start the bot

1. Clone the repo: `git clone https://github.com/dcs-community/binarycoffee_bot.git`
2. Create environment: `virtualenv -p python3 env`
3. Activate environment: `source env/bin/activate`
4. Set environment variables
5. Install packages: `pip install -r requirements.txt`
6. Finally, run `python bot.py`

### Deploy in Heroku

See [this post](https://binary-coffee.dev/post/aprende-a-desplegar-un-bot-de-telegram-en-heroku) for help.

### Setup with docker

1. Clone the repo: `git clone https://github.com/dcs-community/binarycoffee_bot.git`
2. Set environment variables
3. Start docker-compose: `docker-compose up -d`

## Contribution

Any contribution is welcome.

## License

Check our [LICENCE.md](https://github.com/dcs-community/binarycoffee_bot/blob/master/LICENSE) file.
