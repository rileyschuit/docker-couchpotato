[![Build Status](https://travis-ci.org/rileyschuit/rpi-docker-couchpotato.svg?branch=master)](https://travis-ci.org/rileyschuit/rpi-docker-couchpotato) 
  
#Docker couchpotato to run on a Raspberry Pi  
This is a Dockerfile to set up "CouchPotato" - (https://couchpota.to/)  
### Build from docker file  
```
git clone https://github.com/timhaak/docker-couchpotato.git
cd docker-couchpotato
docker build -t couchpotato .
```

### Pull from docker hub:  
```
docker run -d \
    -h *your_host_name* \
    -v /*your_config_location*:/config \
    -v /*your_videos_location*:/data \
     -p 5050:5050 \
    --restart=always \
    --name=couchpotato couchpotato
```
