Criando um container com uma aplicação em NodeJs com Mysql e publicando o acesso com o Nginx. 

O objetivo principal é que quando um usuário acesse o `nginx`, o mesmo fará uma chamada em nossa aplicação `Node.js` em um outro container. Essa aplicação por sua vez adicionará um registro em nosso banco de dados `Mysql`, cadastrando um nome na tabela `people`.

O retorno da aplicação Node.js para o nginx deverá ser:

```html
<h1>Full Cycle Rocks!</h1>
#	Name
```
           
1. Primeiro você deve criar uma network para que os containers possam se comunicar entre si:

```bash
docker network create desafio
```

2. Agora basta executar o comando `docker-compose` para subir os containers:

```bash
docker-compose up -d
```

3. Agora basta acessar a aplicação em seu browser:

```bash
http://localhost:8080
```

Todas as vezes que você atualizar a página, um novo nome será adicionado ao banco de dados. 

4 . Para finalizar os containers:

```bash
docker-compose down
```