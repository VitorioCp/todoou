# Todoou

## decisões tomadas durante o desenvolvimento.

Durante o desenvolvimento do sistema, enfrentei diversos desafios, especialmente na gestão e edição de grupos de tarefas e tarefas individuais. 
Uma das abordagens que implementei foi a utilização de modais para permitir a edição e manipulação dos elementos diretamente na interface. No entanto, 
um grande desafio foi garantir o relacionamento correto entre o ID do grupo de tarefas e as tarefas associadas.
Particularmente, tive que assegurar que, ao deletar um grupo de tarefas, todas as tarefas associadas a esse grupo fossem automaticamente removidas.
Para facilitar futuras alterações no banco de dados e garantir uma maior flexibilidade, optei por utilizar o Sequelize como ORM.


---

### Primeiros Passos

### 1. Clonar o Repositório

Clone o repositório do projeto usando o comando:

```git clone https://github.com/VitorioCp/todoou/```

---

### 2. Está usando o docker para rodar o seu banco de dados

Crie seu bando de dados usando o comando:

```docker run --name mysql -e MYSQL_ROOT_PASSWORD=docker -e MYSQL_USER=docker -e MYSQL_PASSWORD=docker -e MYSQL_DATABASE=mysql -p 3306:3306 -v C:\data:/var/lib/mysql --restart always -d mysql:latest```

Configure o arquivo .env na raiz ```backend/```, para está recebendo DB_NAME, DB_USER, DB_PASS, DB_HOST, DB_PORT, DB_DIALECT, JWT_SECRET e JWT_EXPIRES_IN
Exemplo: 
```
DB_NAME=mysql
DB_USER=docker
DB_PASS=docker
DB_HOST=localhost
DB_PORT=3306
DB_DIALECT=mysql

JWT_SECRET=fwbwqef
JWT_EXPIRES_IN=1h
```
### Observação: para facilitar o uso do sistema, o arquivo já vai está sendo enviado e configurado, com base no codigo fornecido para criar um bando de dados

---

### 3. Instalar Dependências
Acesse os seguintes diretórios e instale as dependências:

### Front end:
```todoou\frontEnd\```

### Back end:
```todoou\backend\```

Execute em ambos o comando:
```npm i```

---

### 4. Executar o Projeto
Após instalar as dependências, inicie o frontend e o backend com os seguintes comandos:

### Front end:
```todoou\frontEnd\```

### Back end:
```todoou\backend\```

### Observação
Certifique-se de que o banco de dados MySQL esteja em execução no Docker. Com o frontend e o backend em execução, o sistema estará funcionando em seu computador.

---

## Tecnologias Utilizadas

### Front End

- React vite
- Axios
- react-router-dom
- styled-components
- react-icons

### Back end

- express
- cors
- sequelize
- jsonwebtoken
- nodemon
- dotenv
- bcrypt
- mysql2


