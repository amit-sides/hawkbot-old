# Plugins

Hawkbot provides the ability to dynamically load different plugins as desired by the user's strategy.
A plugin has full access to any data & functionality provided by the core. Any relevant desired objects (like orderbook, exchange etc)
will be automatically injected by the framework if defined as a variable.

There are several plugins provided by default in Hawkbot, but custom plugins can be added by providing the desired 
plugin in the `user_data/plugins` folder. The following plugins are provided by Hawkbot by default:

* Clustering support/resistance
* DCA
* Gridstorage
* GTFO
* Orderbook TP
* Profit transfer
* Rest server
* Score storage
* Stoploss
* Timeframe support/resistance
* TP
* TP refill
* Wiggle

Below you can find a description of (some of) the plugins on what they are about.

## Gridstorage plugin

The Gridstorage plugin provides a way to store DCA quantities and prices in a database for future reference.  
It is up to the calling party
to indicate what data is to be stored, and when it needs to be reset.

By default, the Gridstorage plugin writes the data to a file gridstorage_plugin.db in the current working directory.  
This location can be overriden via the config file using the following snippet:

    "plugins": {
        "GridStoragePlugin": {
            "database_path": "gridstorage_plugin.db"
        }
    }