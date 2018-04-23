## Criar container
Para criar um container usa-se o comando run com o nome da imagem que será utilizada para a criação:

```sh
docker run NOME_IMAGEM
```

Mas após sua criação o container irá morrer, para manter o container conectado basta adicionar 'bash' no fim do comando

## Listar containers
Sempre que o comando run é executado, o Docker vai criar um container do zero e armazenar para ser utilizado no futuro. O comando run não deve ser utilizado toda hora, por isso para listar os containers que já existem é usado 'ps'

```sh
docker ps
```

## Rodar containers Docker que já foram criados

```sh
docker start NOME_CONTAINER
```

O comando start funciona apenas com containers.

## Acessar containers que já estão rodando
Usa-se o comando 'attach'
```sh
docker attach NOME_CONTAINER
```

