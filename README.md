# Minecraft Server hosted in docker

This project allows you to host your minecraft server inside docker and without opening ports on your router thanks to ngrok.

Pre-requisites : `docker`, `docker-compose` (included in docker desktop), a [ngrok](https://ngrok.com/) account

## Get ngrok authtoken

Once you have a ngrok account, you can find your auth-token [here](https://dashboard.ngrok.com/get-started/your-authtoken).

Put the auth token inside a .env file:

echo 'NGROK_TOKEN=your_authtoken' > .env

## Review server settings

In the [docker-compose.yml](docker-compose.yml) file, you can now review the settings for the minecraft server : the Ops list, the maximum of players, etc..

## Launch server

```
docker-compose up -d
```


When you are finished, to close the server :

```
docker-compose down
```

## Get the IP address of the server :

Go to [localhost:4040](localhost:4040)

Your IP address is the showed link without the prefix "tcp://"

(example: 1.tcp.eu.ngrok.io:12345)
