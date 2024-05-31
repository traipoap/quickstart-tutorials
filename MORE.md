Add on profile of services
```yaml
volumes:
- /var/run/docker.sock:/var/run/docker.sock # socket
- /usr/bin/docker:/usr/bin/docker # docker
```

### Add on agent of dockerfile
```Dockerfile
RUN curl -SL https://github.com/docker/compose/releases/download/v2.26.1/docker-compose-linux-x86_64 -o /usr/local/bin/docker-compose
RUN chmod +x /usr/local/bin/docker-compose
RUN docker-compose --version
```

### Add on agent
```bash
chown jenkins:jenkins /var/run/docker.sock
```