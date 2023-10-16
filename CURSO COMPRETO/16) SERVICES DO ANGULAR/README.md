# SERVICES DO ANGULAR
Em Angular, os serviços são uma parte fundamental da arquitetura de um aplicativo. Os serviços são usados para separar a lógica de negócios e as funcionalidades reutilizáveis do restante do aplicativo, como componentes e diretivas. Eles oferecem um local centralizado para compartilhar dados, executar operações assíncronas, acessar APIs externas e muito mais. Aqui está o que você precisa saber sobre os serviços no Angular:

1. **Criação de Serviços**:
   - Para criar um serviço, você pode usar o Angular CLI para gerar automaticamente um arquivo de serviço. Isso é feito com o comando `ng generate service nome-do-servico`. O serviço resultante será uma classe TypeScript que contém a lógica de negócios específica.

2. **Injeção de Dependência**:
   - Os serviços são injetados em componentes, diretivas e outros serviços usando a injeção de dependência. Isso significa que você pode declarar uma dependência de serviço no construtor do componente e o Angular cuidará da criação da instância do serviço e da injeção no componente.

   Exemplo de injeção de dependência em um componente:
   ```typescript
   import { MeuServico } from './meu-servico.service';

   @Component({
     selector: 'app-meu-componente',
     template: '...',
   })
   export class MeuComponenteComponent {
     constructor(private meuServico: MeuServico) {
       // Agora você pode acessar o serviço aqui
     }
   }
   ```

3. **Escopo do Serviço**:
   - Por padrão, os serviços no Angular têm um escopo de aplicação, o que significa que uma única instância do serviço é compartilhada entre todos os componentes que injetam o serviço. Isso é útil para compartilhar dados e estado entre componentes.

4. **Utilidades dos Serviços**:
   - Os serviços são úteis para realizar tarefas como acesso a APIs externas, manipulação de dados, gerenciamento de estado, autenticação, validação, entre outras tarefas de lógica de negócios. Eles também são ideais para isolar a lógica de apresentação dos componentes, tornando o código mais limpo e fácil de testar.

5. **Injeção de Outros Serviços**:
   - Os serviços podem injetar outros serviços, o que permite criar uma hierarquia de serviços. Isso é útil para organizar a lógica do aplicativo em serviços modulares e reutilizáveis.

6. **Testabilidade**:
   - O uso de serviços facilita a realização de testes unitários, pois você pode substituir os serviços reais por versões de simulação (mocks) durante os testes. Isso permite que você teste componentes independentemente da lógica de negócios do serviço.

7. **Serviços Angular Internos**:
   - O Angular possui serviços internos embutidos, como o `HttpClient` para fazer solicitações HTTP, o `Router` para gerenciar navegação e o `ActivatedRoute` para acessar os parâmetros de roteamento.

Os serviços são uma parte essencial do desenvolvimento de aplicativos Angular. Eles ajudam a manter o código organizado, promovem a reutilização, simplificam a injeção de dependência e tornam o aplicativo mais testável. Ao separar a lógica de negócios em serviços, você cria um aplicativo mais modular e escalável.