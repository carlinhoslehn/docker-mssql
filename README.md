# Container MSSQL Microsoft
Docker MSSQL utilizando a image original disponibilizada pela microsoft.
O Exemplos usados abaixo é para usar o docker no linux, caso esteja  usando windows, você pode conferir [Docker Hub Microsoft](https://hub.docker.com/r/microsoft/mssql-server-windows-developer/)
### Como rodar?!
Para utilizar essa Docker você precisa ter instalado o docker compose, 
Para subir o container use:
```sh
$ docker-compose up
```
Caso não tenha o docker compose pode erguer o bloco da seguinte forma:
```sh
$ docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=1234567890' -p 1433:1433 -v /pasta_local_teu_pc/.db:/var/opt/mssql -d mcr.microsoft.com/mssql/server:2017-latest
```

Lembrando que caso não queira a persistencia de dados do banco você pode utilizar
somente o comando:
```sh
$ docker run -e 'ACCEPT_EULA=Y' -e 'MSSQL_SA_PASSWORD=1234567890' -p 1433:1433 -d mcr.microsoft.com/mssql/server:2017-latest
```
