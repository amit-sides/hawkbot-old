## Requirements

The bot requires Python 3.8 or later.

`requirements.txt` contains the dependancies.


## Quick startup procedure

* (If desired, create and activate a virtual environment)
* Install the requirements: `pip install -r requirements.txt`
* Copy the example account from `user_data/account.example.json` into `user_data/account.json` and adjust it by entering API key and secret
* Copy the example config from `user_data/config.example.basic.json` into `user_data/config.json` and adjust it by entering exchange and the symbols config 
* Launch the bot with `python3 trade.py`

## The account file

The account file specifies the api key and secret per exchange.  
It can contain multiple exchange configurations, and the exchange specified in the config file 
defines which account information is actually used.

## The config file

Some example strategies are available here: [/config-samples](../user_data/config-samples/)  
The config file is split into global settings and symbol specific config: