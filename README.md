# GameSurge website

[![Build Status](https://travis-ci.org/GameSurge/web.svg?branch=master)](https://travis-ci.org/GameSurge/web)

## Development

### Install

- Clone the repo and `cd` to it
- `pyvenv-3.5 .venv`
- `pip install -r requirements.txt`
- `pip install -e .`
- `npm install`
- `cp gsweb/defaults.cfg gsweb.cfg`
- Set a `SECRET_KEY` in gsweb.cfg and change `SQLALCHEMY_DATABASE_URI` if necessary
- Create a Postgres database, e.g. using `createdb gsweb`


### Enable code style checks

- Install eslint and sass-lint so it's in your PATH (e.g. `sudo npm install -g eslint sass-lint`)
- `pip install pep8`
- `ln -sr pre-commit.githook .git/hooks/pre-commit`

If you do not want to install eslint globally you can also install it locally,
copy the git hook instead of symlinking it and point the `ESLINT_CMD` variable
in the script to the local eslint (e.g. `node_modules/.bin/eslint`).  
The same applies to sass-lint (`SASSLINT_CMD`)



### Run
- `export FLASK_APP=gsweb._cliapp FLASK_DEBUG=1 GSWEB_CONFIG=/path/to/your/gsweb.cfg`
- `flask createdb` (creates tables in the database)
- `flask gulp` (monitors and rebuilds assets)
- `flask run --with-threads`

_   _                 _                        
| |_| |__   __ _ _ __ | | __  _   _  ___  _   _ 
| __| '_ \ / _` | '_ \| |/ / | | | |/ _ \| | | |
| |_| | | | (_| | | | |   <  | |_| | (_) | |_| |
 \__|_| |_|\__,_|_| |_|_|\_\  \__, |\___/ \__,_|
                              |___/             


