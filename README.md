# minima-docker

## Auto add user
```
wget -O minimad.sh https://raw.githubusercontent.com/Megumiiiiii/minima-docker/main/minimad.sh && chmod +x minimad.sh && ./minimad.sh
```

## Run
```
docker run -d -e minima_mdspassword=123 -e minima_server=true -v ~/minimadocker9001:/home/minima/data -p 9001-9004:9001-9004 --restart unless-stopped --name minima9001 minimaglobal/minima:latest
```

## Auto update
```
docker run -d --restart unless-stopped --name watchtower -e WATCHTOWER_CLEANUP=true -e WATCHTOWER_TIMEOUT=60s -v /var/run/docker.sock:/var/run/docker.sock containrrr/watchtower
```
