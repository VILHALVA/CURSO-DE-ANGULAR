# INSTALANDO O ANGULAR - PRIMEIRO PROJETO
## INICIO:
Para instalar o Angular em seu ambiente de desenvolvimento, você precisará usar o Angular CLI (Command Line Interface), que é uma ferramenta oficial para criar e gerenciar projetos Angular. Siga as etapas abaixo para instalar o Angular CLI:

**Passo 1: Instale o Node.js:**

O Angular CLI requer o Node.js para funcionar. Se você ainda não o tem instalado, siga estas etapas:

1. Acesse o site oficial do Node.js: https://nodejs.org/.
2. Faça o download da versão LTS (Long Term Support), que é recomendada para a maioria dos desenvolvedores.
3. Execute o instalador e siga as instruções para concluir a instalação.

**Passo 2: Instale o Angular CLI:**

Após ter o Node.js instalado, você pode instalar o Angular CLI usando o npm (gerenciador de pacotes do Node.js). Abra o terminal ou prompt de comando e digite o seguinte comando:

```
npm install -g @angular/cli
```

Isso instalará o Angular CLI globalmente no seu sistema. O `-g` indica que a instalação é global.

**Passo 3: Verifique a instalação:**

Para verificar se a instalação foi bem-sucedida, digite o seguinte comando:

```
ng --version
```

Isso deve exibir a versão do Angular CLI e outras informações relacionadas.

Agora, você tem o Angular CLI instalado e está pronto para criar projetos Angular e começar a desenvolver. Para criar um novo projeto Angular, você pode usar o seguinte comando:

```
ng new nome-do-seu-projeto
```

Substitua "nome-do-seu-projeto" pelo nome que você deseja dar ao seu projeto. O Angular CLI irá orientá-lo através de várias opções de configuração.

Depois de criar seu projeto, você pode entrar no diretório do projeto usando `cd nome-do-seu-projeto` e, em seguida, usar o comando `ng serve` para iniciar um servidor de desenvolvimento e visualizar seu aplicativo em seu navegador.

Lembre-se de que a instalação do Angular CLI e a criação de um novo projeto são tarefas únicas. Depois disso, você pode usar o projeto existente para desenvolver seu aplicativo Angular.

## ERROS QUE PODEM OCORRER:
**Relatório sobre a Instalação do Angular:**

No contexto da instalação do Angular, o processo envolveu várias etapas e resolução de problemas para garantir que o ambiente de desenvolvimento esteja configurado corretamente. Aqui estão os principais pontos do relatório:

1. **Preparação do Ambiente:**
   - Antes de iniciar a instalação do Angular, foi necessário preparar o ambiente de desenvolvimento. Isso envolveu a instalação do Node.js, que é uma plataforma necessária para a execução do Angular CLI, e a instalação do Visual Studio Code, que é uma escolha popular de ambiente de desenvolvimento para trabalhar com Angular.

2. **Instalação do Angular CLI:**
   - O Angular CLI (Command Line Interface) foi instalado usando o comando `npm install -g @angular/cli`. Isso permitiu o uso do Angular CLI globalmente no sistema, facilitando a criação e gerenciamento de projetos Angular.

3. **Problemas de Dependências:**
   - Durante a instalação das dependências do projeto usando o comando `npm install`, foram observados alguns avisos relacionados a dependências desatualizadas e vulnerabilidades. Esses avisos são comuns ao trabalhar com projetos Node.js e podem ser resolvidos examinando as vulnerabilidades relatadas e tomando medidas apropriadas para corrigi-las.

4. **Execução do Servidor de Desenvolvimento:**
   - Após a instalação bem-sucedida das dependências e resolução de eventuais problemas, o servidor de desenvolvimento do Angular foi iniciado com êxito usando o comando `ng serve`. O servidor está configurado para ouvir em `http://localhost:4200/`, permitindo a visualização em tempo real do aplicativo Angular durante o desenvolvimento.

5. **Conclusão:**
   - Com o servidor de desenvolvimento em execução, o ambiente está pronto para o desenvolvimento de aplicativos Angular. Qualquer problema inicial relacionado à instalação foi resolvido com sucesso, e o desenvolvimento pode prosseguir.

**Observações Finais:**
- É importante estar atento a avisos e vulnerabilidades em dependências e considerar a execução do comando `npm audit` para obter detalhes adicionais.
- Mantenha-se atualizado com as melhores práticas de segurança e atualize as dependências conforme necessário para manter um ambiente de desenvolvimento seguro.

Este relatório resume as etapas de instalação do Angular e as questões encontradas ao longo do processo. 