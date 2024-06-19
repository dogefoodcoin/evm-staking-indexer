# EVM Staking Indexer

## Indexer
### Config
Modify the config file `indexer/config.toml`
### Run
```
./indexer
```
## Scanner
### Set env vars
```
export DATABASE_URL=postgres://{user}:{password}@{host}/{db}
```
Use `scanner/schema.sql` to create tables in DB.
### Run
```
./scanner --node <node RPC> --start <block number> --interval <interval>
```
* `node` is required.
* `start` is not required, starting from `4636000` by default.
* `interval` is not required, default value is `15` in seconds.
## Updater
### Config
Modify the config file in `updater/config.toml`
### Run
```
./updater
```