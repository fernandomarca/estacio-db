## Conteiner configurado para aulas de Implementação de Banco de Dados


### Pré-riquisito ter docker e docker-compose instalados em seu sistema independente se for windowns, linux ou mac ou até mesmo o wsl no windows.

### Pode ser instalado em seu sistema seguindo a documentação oficial: 
  - https://www.docker.com/get-started

### Pela primeira vez dentro do diretório postgres no terminal: 

   - rode o comando

  ```bash
      docker-compose build
  ```

   - Isso cria o container com o postgres e o pgadmin 4.

### Na sequencia rode:

  ```bash
      docker-compose up
  ```
  Isso de fato inicializa o postgres e pgadmin.
  O Postgres está rodando na porta padrão 5432.
  A senha do usuário "postgres" é "senha" a mesma do professor.

### Acessando o pgadmin no brower, simplismente digite o endereço abaixo no navegador

  - http://localhost:9000
  - Na tela inicial faça o login com: 
    - login: admin@user.com
    - senha: 123456

### Criando a conexão com o postgres
  1 - clique com o botão direito em servers, e selecione Register e clique em Server...
  ao abrir a janela General coloque o name como: postgresql14.

  ![dbml](https://github.com/fernandomarca/estacio-db/print/register.png)

  2 - Na aba Connetion entre com as informações conforme o print abaixo:
    - Para o host: database (esse é o nome do serviço no container)
    - username: postgres
    - password: senha

  ![dbml](https://github.com/fernandomarca/estacio-db/print/connection.png)

### Pronto seguindo esses passos está tudo configurado, siga com a aula.

### Se você não faz a minima ideia do que é Docker e docker-compose sugiro que leia a documentação oficial para a instalação e para conhecer do que se trata.
  - https://www.docker.com/get-started

### Para matar o container ctrl+c ou em um segundo terminal rode:

  ```bash
      docker-compose stop
  ```