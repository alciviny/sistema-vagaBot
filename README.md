# Sistema VagaBot

Backend para o sistema de automação de vagas.

## Estrutura de Pastas

O projeto utiliza uma arquitetura baseada em Serviços, Rotas e Controladores, semelhante ao padrão MVC, para organizar o código de forma clara e escalável.

- **`/src`**: Contém todo o código-fonte da aplicação.

  - **`/config`**: Arquivos de configuração. Ideal para armazenar configurações de conexão com banco de dados, chaves de API e outras variáveis de ambiente.

  - **`/controllers`**: Responsáveis por receber as requisições das rotas, processar os dados de entrada (validar, etc.), chamar os serviços apropriados e retornar uma resposta ao cliente.

  - **`/middlewares`**: Funções executadas entre o recebimento da requisição e a chegada ao controlador. Usado para tarefas como autenticação, autorização, logging, etc.

  - **`/models`**: Define a estrutura e o esquema dos dados (por exemplo, Schemas do Mongoose para o MongoDB). É a representação de como os dados são armazenados no banco de dados.

  - **`/routes`**: Define todos os endpoints (URLs) da API. Mapeia cada rota para o seu respectivo controlador.

  - **`/services`**: Contém a lógica de negócio principal e mais complexa da aplicação. Os controladores chamam os serviços para executar tarefas específicas (ex: criar um usuário, processar um pagamento). Isso ajuda a manter os controladores mais limpos e a reutilizar código.

  - **`/views`**: Para aplicações que renderizam o front-end no servidor, esta pasta conteria os arquivos de visualização (HTML, EJS, Pug, etc.). Para uma API REST pura, esta pasta pode não ser utilizada.
