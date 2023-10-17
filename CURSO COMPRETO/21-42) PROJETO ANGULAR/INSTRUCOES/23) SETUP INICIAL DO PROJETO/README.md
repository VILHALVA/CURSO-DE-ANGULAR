# SETUP INICIAL DO PROJETO
O setup inicial de um projeto Angular envolve a configuração do ambiente de desenvolvimento e a criação de um novo projeto Angular. Aqui estão os passos gerais para configurar um projeto Angular:

1. **Instale o Node.js:**
   Antes de começar, certifique-se de que o Node.js esteja instalado no seu sistema. Você pode baixar a versão mais recente do Node.js em [nodejs.org](https://nodejs.org/). O Node.js é necessário para o gerenciamento de pacotes e para executar o Angular CLI.

2. **Instale o Angular CLI:**
   O Angular CLI (Command Line Interface) é uma ferramenta que facilita a criação, desenvolvimento e implantação de aplicativos Angular. Para instalar o Angular CLI globalmente, execute o seguinte comando no seu terminal:

   ```sh
   npm install -g @angular/cli
   ```

3. **Crie um Novo Projeto Angular:**
   Use o Angular CLI para criar um novo projeto Angular. Navegue para o diretório onde você deseja criar o projeto e execute o seguinte comando:

   ```sh
   ng new nome-do-projeto
   ```

   Siga as instruções para configurar o projeto, como a escolha de opções de estilo, roteamento e mais.

4. **Navegue para o Diretório do Projeto:**
   Após a conclusão da criação do projeto, navegue para o diretório do projeto com o comando:

   ```sh
   cd nome-do-projeto
   ```

5. **Inicie o Servidor de Desenvolvimento:**
   Inicie o servidor de desenvolvimento com o comando:

   ```sh
   ng serve
   ```

   Isso iniciará o servidor de desenvolvimento e seu aplicativo estará acessível no navegador em `http://localhost:4200/`. O servidor atualizará automaticamente o aplicativo quando você fizer alterações nos arquivos.

6. **Comece a Desenvolver:**
   Agora você está pronto para começar a desenvolver seu projeto Angular. Os arquivos do projeto estão localizados no diretório `src`. Você pode começar a criar componentes, serviços e outros recursos conforme necessário.

7. **Outras Configurações Opcionais:**
   Dependendo dos requisitos do seu projeto, você pode configurar rotas, estilos, integração com APIs e outras funcionalidades específicas.

Lembre-se de que o Angular CLI simplifica muitas das tarefas de configuração, como a criação de componentes, serviços e módulos, tornando o desenvolvimento mais eficiente.

Este é um guia básico para o setup inicial de um projeto Angular. À medida que você avança no desenvolvimento, pode precisar configurar outras dependências ou ferramentas específicas para o seu projeto. Certifique-se de consultar a documentação oficial do Angular (https://angular.io) para obter informações detalhadas sobre como configurar e desenvolver aplicativos Angular.