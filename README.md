## How to use this image

Use this command to start the container. Zabbix proxy will listen on port 10051.
```
docker run \
	--name zabbix-proxy \
	-d \
	-p 10051:10051 \
	mher718/zabbix-proxy \
-z <zabbix server fqdn or ip> \
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
