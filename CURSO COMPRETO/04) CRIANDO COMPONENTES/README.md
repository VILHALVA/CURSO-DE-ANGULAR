# CRIANDO COMPONENTES
Criar componentes é uma parte fundamental do desenvolvimento de aplicativos Angular. Os componentes são os blocos de construção de uma aplicação Angular e representam partes reutilizáveis e independentes da interface do usuário. Aqui estão as etapas para criar um novo componente em um projeto Angular:

1. **Usar o Angular CLI**:
   O Angular CLI torna a criação de componentes rápida e fácil. Você pode usar o seguinte comando para gerar um novo componente:

   ```
   ng generate component nome-do-seu-componente
   ```

   Certifique-se de substituir "nome-do-seu-componente" pelo nome do componente que você deseja criar. O Angular CLI criará automaticamente os arquivos necessários para o componente, além de adicionar automaticamente a referência do novo componente ao módulo apropriado.

2. **Estrutura do Componente**:
   Após a criação bem-sucedida do componente, você encontrará os seguintes arquivos na pasta do componente:

   - `nome-do-seu-componente.component.ts`: Este é o arquivo TypeScript que contém a lógica do componente, incluindo a classe do componente.
   - `nome-do-seu-componente.component.html`: Este é o arquivo de modelo HTML que define a estrutura da interface do usuário do componente.
   - `nome-do-seu-componente.component.css` (opcional): Este é o arquivo de estilos CSS específicos do componente.
   - `nome-do-seu-componente.component.spec.ts`: Este é o arquivo de teste unitário do componente, usado para testar o comportamento do componente.

3. **Personalizar o Componente**:
   Você pode personalizar o componente de acordo com as necessidades do seu aplicativo. Isso pode incluir a adição de elementos HTML, estilos CSS, lógica de negócios e manipuladores de eventos.

4. **Usar o Componente em Templates**:
   Uma vez que o componente tenha sido criado e personalizado, você pode usá-lo em templates HTML de outros componentes ou em arquivos de roteamento para exibir o conteúdo do componente. Use a tag do componente no HTML de outro componente para incluir o novo componente na interface do usuário.

5. **Registrar o Componente no Módulo**:
   Certifique-se de registrar o novo componente no módulo apropriado do seu aplicativo. Isso envolve adicionar o componente à matriz `declarations` no decorator `@NgModule` do módulo. Isso permitirá que o Angular reconheça e use o componente.

6. **Executar o Aplicativo**:
   Após criar e configurar o componente, você pode executar o aplicativo com o comando `ng serve`. Isso iniciará o servidor de desenvolvimento, permitindo que você visualize o aplicativo e o novo componente no navegador.

Ao seguir essas etapas, você pode criar, personalizar e usar componentes para construir a interface do usuário do seu aplicativo Angular. Componentes são essenciais para a criação de aplicativos modulares, reutilizáveis e bem organizados. Você pode criar tantos componentes quantos forem necessários para atender aos requisitos do seu aplicativo.