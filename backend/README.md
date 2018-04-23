## Criar DockerFile
Após ter o DOCkER instalado em seu pc, crie na pasta de seu projeto o arquivo DockerFile e abra um editor de texto passando
os seguintes códigos:

```sh
## qual imagem está sendo utilizada
FROM mysql:latest

## criar o banco quando der star no container
COPY ./demo.sql /docker-entrypoint-initdb.d/
```

## Inicializando o Banco de Dados
Aqui é necessário colocar o comando a seguir, passando o nome do banco, o camando MYSQL_ALLOW_EMPTY_PASSWORD, permitindo o uso de senhas
vazias(yes), --NAME indicando o nome do container e depois a imagem que vai rodar e qual sua versão

```sh
docker run -d -e MYSQL_DATABASE='demo' -e MYSQL_ALLOW_EMPTY_PASSWORD='yes' --name backend db:0.0.1
```

## Log do Container


Para saber qual o log do container que está rodando, deve-se:

```sh
docker logs nome_container

exemplo: 

docker logs backend
```

## Executando comando dentro do container
Executar um comando que está sendo rodado e entrar no BD.
```sh
docker exec -ti backend mysql -u root -p
```

## Juntando FRONTEND e BACKEND

Para fazer esse junção necessita do seguinte comando:
```sh
docker run -d -p 80:80 --name frontend --link backend frontend:0.0.1
```
Devemos rodar o front, e então mostrar o conteúdo na porta 80:80, dar um nome, no caso (frontend), linkar com o container de backend,
informando que devem se comunicar entre si e após isso informar o nome da imagem e sua versão.




