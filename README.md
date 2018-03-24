# servidor
IaC da infra do Raul

### Dependência

- [docker]()
- [docker-compose]() 

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