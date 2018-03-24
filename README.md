# servidor
IaC da infra do Raul

### Dependência

- [docker](https://docs.docker.com/install/linux/docker-ce/debian/#install-docker-ce-1)
- [docker-compose](https://docs.docker.com/compose/install) 
- ansible-vault

### Instalando ansible vault

```
apt-get install python-pip -y
pip install ansible-vault
```

### Manipulando o arquivo criptografado

Pegue a senha do vault e digite esse comando

Para decriptografar

```
ansible-vault decrypt ./config/postfix-virtual.cf
```

Para encryptar 

```
ansible-vault encrypt ./config/postfix-virtual.cf
```

**POR FAVOR!! LEMBRE-SE DE ENCRIPTAR ANTES DE MANDAR PRO GITHUB**

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