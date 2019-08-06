Haven
====

**Hello world level demo, work in progress**

## Requirements

- Ubuntu 18.04
- Intel SGX driver 2.5
- Intel SGX SDK 2.5
- Rust nightly 2019-05-22

## Installation

- Clone the repo
- `git submodule init`
- `git submodule update`
- `make`
- make sure put `spid.txt` and `key.txt` into `bin/`, the SPID must be linkable
- `cd bin`
- `./app`

## API endpoints

POST `/register`

```json
{
  "input": {},
  "nonce": {
    "foo": "bar"
  }
}
```

POST `/status`

```json
{
  "input": {
    "account": ""
  },
  "nonce": {
    "foo": "bar"
  }
}
```

POST `/transfer`

```json
{
  "input": {
    "sk": "",
    "to_account": "",
    "quantity": 100
  },
  "nonce": {
    "foo": "bar"
  }
}
```

POST `/dump_sessions`

```json
{
  "input": {},
  "nonce": {
    "foo": "bar"
  }
}
```

POST `/load_sessions`

```json
{
  "input": {
    "data": "",
    "nonce": ""
  },
  "nonce": {
    "foo": "bar"
  }
}
```
