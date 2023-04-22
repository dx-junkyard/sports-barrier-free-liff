# sports-barrier-free-liff

## Install

### ssl (mac)

```sh
$ brew install mkcert
$ mkcert -install  # optional

$ cd sports-barrier-free-liff
$ mkcert localhost
```

verify `localhost-key.pem` and `lcoalhost.pem` were created on app root


### .env content

create file `.env` file on root with following content

```env
NEXT_PUBLIC_LIFF_ID="xxxx"
NEXT_PUBLIC_PB_HOST="http://127.0.0.1:8090"
NEXT_PUBLIC_PB_ADMIN_EMAIL="admin@example.com"
NEXT_PUBLIC_PB_ADMIN_PASSWORD="admin_password"
NEXT_PUBLIC_PB_USER_DEFAULT_PASSWORD="user_password"
```

## Development

### develop on local

```sh
# developed on nodejs v16
$ yarn install

# use `dev:proxy` for ssl enabled. ssl required for LINE LIFF development
$ yarn dev:proxy
```

open `https://localhost:3001/`


## develop on docker

```sh
docker-compose up
```

open `https://localhost:3001/`

local files are mounted on container except `node_modules`. hot reload could work.

you will need `docker-compose build --no-cache` for any changes on `node_modules`.
