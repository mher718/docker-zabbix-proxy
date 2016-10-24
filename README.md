[![Docker Stars](https://img.shields.io/docker/stars/safelinkinternet/zabbix-proxy.svg)](https://hub.docker.com/r/safelinkinternet/zabbix-proxy/) [![Docker Pulls](https://img.shields.io/docker/pulls/safelinkinternet/zabbix-proxy.svg)](https://hub.docker.com/r/safelinkinternet/zabbix-proxy/)
# Zabbix proxy on Ubuntu

Total size of this image is:
[![](https://badge.imagelayers.io/safelinkinternet/zabbix-proxy:latest.svg)](https://imagelayers.io/?images=safelinkinternet/zabbix-proxy:latest 'Get your own badge on imagelayers.io')


## Running

Use this command to start the container. Zabbix proxy will listen on port 10051.
```
docker run \
	--name zabbix-proxy \
	-d \
	-p 10051:10051 \
	safelinkinternet/zabbix-proxy \
  -z <zabbix server ip> \
  -s <proxy hostname>
```
________________________________________

### Configuration
**Parameters**
    REQUIRED:
      `-s, --host`           Zabbix hostname to use for Zabbix proxy (Hostname= in conf).
      `-z, --zabbix-server`  Zabbix server IP or DNS name (Server= in zabbix_proxy.conf).
    OPTIONAL:
      `-m, --monit`          Command to pass to Monit {start|stop|restart|shell|status|summary}. Default: run
      `-p, --port`           Zabbix server port to send to (ServerPort= in zabbix_proxy.conf). Default: 10051


#### Explore running container

    `docker exec -it zabbix-proxy bash`
