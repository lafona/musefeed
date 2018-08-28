### Supported Exchanges
* Openledger (BTS-OPEN.XSD)

### Setup and Running on ubuntu 16.04

sudo apt install virtualenv libffi-dev libssl-dev python-dev  
virtualenv -p /usr/bin/python3 venv  
source venv/bin/activate  
git clone https://github.com/xeroc/piston-lib.git  
cd piston-lib/  
git checkout 0.4.1  
pip install -e . 
cd ..  
pip install python-dateutil  
git clone https://github.com/lafona/musefeed.git  
cd musefeed  
git checkout musefeed  

_edit musefeed.py to correct witness name_


python musefeed.py #needs to be running with cli wallet open and unlocked in another window './cli_wallet -r'  


### Additional Configuration Info
Then, edit the `steemfeed.py` to configure. We have some items under Config category in the code.

* `interval`: Interval of publishing price feed. The default value is one hour (3600 seconds)
* `freq`: Frequency of parsing trade history.
* `min_change`: Minimum price change percentage to publish feed
* `max_age`: Maximum age of price feed
* `manual_conf`: Maximum price change without manual confirmation. If price change exceeds this, you will be asked to confirm
* `use_telegram`: If you want to use Telegram for confirmation, enter 1
* `telegram_token`: Create your Telegram bot at @BotFather (https://telegram.me/botfather)
* `telegram_id`: Get your telegram id at @MyTelegramID_bot (https://telegram.me/mytelegramid_bot)
* `bts_ws` : List of BitShares Websocket servers
* `rpc_host`: Your RPC host address
* `rpc_port`: Your RPC host port
* `witness`: Enter ***YOUR WITNESS ID***
