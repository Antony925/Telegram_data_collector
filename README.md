# Telegram data collector v0.02
Combination of tools to download your telegram data.


### Structure
##### 0_download_dialogs_list.py
Download dialogs meta data for account.

`--dialogs_limit` - means number of dialogs

`-h` - show this help message and exit

`--config_path` - path to your config file ()

`--debug_mode` - Debug mode


##### 1_download_dialogs_data.py
Downloads all messages from the dialogs.

Use flags `--skip_private`, `--skip_groups`, and `--skip_channels`
to skip private chats, groups, and channels respectively.

### Requirements
Python 3.8.13


### How to run
0. Open your command prompt as administrator
1. create virtual env
```python -m venv .venv```
2. activate virtual env
```. .venv/bin/activate```
3. install dependencies 
```pip install -r requirements.txt```
4. get your credentials https://my.telegram.org/apps
5. set credentials (api_id, api_hash) in *config/config.json* (can be based on the *config_example.json*)

### How to start
0. ```python 0_download_dialogs_list.py --dialogs_limit -1```
1. ```python 1_download_dialogs_data.py --dialogs_ids -1 --dialog_msg_limit -1```
