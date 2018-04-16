# Sistemas para Internet - SecDevOps

***nac:*** Criação de uma aplicação no formato "CRUD" executada em containers com base na linguagem "PHP" e no banco de dados "MySQL";

---

***Importante:***

Instruções sobre modelo de execução e entregáveis podem ser obtidas no [diretório de documentação](https://github.com/fiapsecdevops/php-sample-app/tree/master/docs) ou no portal do aluno;

Duvidas podem ser enviadas para <profhelder.pereira@fiap.com.br>

Esta app foi adaptada do exemplo contido [neste artigo](https://www.tutorialrepublic.com/php-tutorial/php-mysql-crud-application.php)

A estrutura foi criada com base nas seguintes tags:

- frontend-0.1: Versão de testes SEM conexão com o banco para a primeira parte da NAC;
- stable:  Versão COM as linhas de conexão com o banco configuradas, será necessário que o MySQL esteja operante para testes faltando apenas a criação do Dockerfile da aplicação/mysql;

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

## Componentes

- Stateful são aplicações que possuem persistência de dados, portanto o Banco de Dados.

- Stateless não possuem persistência de dados como páginas estáticas por exemplo, portanto a parte de front-end.
