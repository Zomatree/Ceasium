# Caesium - Highly Reactive Database
NOTE: This is alpha software and bugs are prone to be in this, please submit issues and PRs to help fix them


## Running
```rust
$ cargo build --release
$ ./target/release/caesium
```

## Using

Connect to websocket for pushing, pulling and events

### Opcodes

```
Receive:
    0 - Identify - Send username and password, if no responce you will get kicked from the websocket
    1 - Heartbeat - Confirms you are still connected, if no responce you will get kicked from the websocket
    2 - Event - for the events you subscribe to (set in the identify)

Send:
    0 - Indentify - Send back username and password, complementry to Recv[0]
    1 - Heartbeat - Confirms you are still connected, complemetry to Recv[1]
    3 - Command - all the db interacts are done though this
```

## TODO

 - [ ] websocket connection
 - [ ] datatypes in rust
 - [ ] background indexer to index all rows
 - [ ] writing to disk
 - [ ] event system for inserts, updates and deletes
 - [ ] encoder and Decoder for websocket
 - [ ] command format for using the database