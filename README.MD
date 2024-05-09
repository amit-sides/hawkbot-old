![logo](docs/img/hawkbot_logo.png)

:warning: **Use at your own risk, you are fully responsible for any risk taken trading. Crypto can be lucrative, but 
is also a high-risk asset class** :warning:

# Overview
Hawkbot is a trading bot that supports trading on different exchanges and markets.

It's built with the intention of being a highly flexible framework that facilitates custom written strategies. 
The main difference between this bot and other trading bots is that it gives full control to the developer, allowing
any strategy you can think of to be created by means of a user-intuitive domain model while still allowing direct 
interaction with the core.

The bot supports running multiple symbols in 1 instance, running futures, spot and supports websockets out of the box.

For further information on how to use the bot, please refer to the [documentation](docs/index.md).

# Support
You can join discord at https://discord.gg/GjZ7Eej2N9

# License
This software is available to use under the EULA specified in the [LICENSE](LICENSE) file.

# Setup

### Docker installation
#### Prerequisites:
- Docker 19.03.0+
- Docker-compose 1.25.5+

#### Steps:
1. Clone the repository and change directory to the root of the repository.
2. Configure account's configurations file and place it in `./configs/account.json`.
3. Configure the bot's configurations file and place it in `./configs/config.json`.
4. Place license file in `./pyarmor.rkey`.
5. Change the account name `bybit_01` in the command line of the `docker-compose.yml` file (last line).
6. Run `docker-compose up -d --build` to start the bot.
   * Additional command line arguments can be added to the bot's command line using the `PARAMS` environment variable.
7. Run `docker-compose logs -f` to view the logs.
   * Use `Ctrl+C` to exit.
   * Use `--tail <number>` to view previous lines.
8. Run `docker-compose down` to stop the bot.