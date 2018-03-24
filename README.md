# servidor
IaC da infra do Raul

### Dependência

- [docker](https://docs.docker.com/install/linux/docker-ce/debian/#install-docker-ce-1)
- [docker-compose](https://docs.docker.com/compose/install) 

### Como usar

```
docker-compose up -d
```

### Adicionando novo alias

Adicione uma nova linha no arquivo [config/postfix-virtual.cf](./config/postfix-virtual.cf)

```
# Forward to external email address
gomex@test.raulhc.cc linux.rafa@gmail.com
``` 

Reinicie o docker

```
docker-compose restart
```