# DYNAMIC ROUTES - SELECIONANDO DADO INDIVIDUAL
Rotas dinâmicas são usadas no Angular quando você deseja exibir informações específicas com base em um identificador (por exemplo, um ID) passado na URL. Isso permite que você crie páginas detalhadas para cada item em uma lista, como uma postagem em um blog ou um produto em uma loja online. Vou mostrar como criar rotas dinâmicas para exibir dados individuais com base em um identificador na URL:

1. **Configuração de Rota**:
   Primeiro, configure suas rotas no arquivo de configuração de rota do Angular (geralmente `app-routing.module.ts`). Crie uma rota dinâmica que aceite um parâmetro, geralmente chamado de `id`.

   ```typescript
   const routes: Routes = [
     { path: 'produtos', component: ListaProdutosComponent },
     { path: 'produto/:id', component: DetalhesProdutoComponent },
   ];
   ```

   Neste exemplo, `produto/:id` é uma rota dinâmica que espera um parâmetro chamado `id` na URL.

2. **No Componente**:
   No componente `DetalhesProdutoComponent`, você deve acessar o parâmetro `id` da rota e usar esse valor para carregar os dados específicos do produto.

   ```typescript
   import { ActivatedRoute } from '@angular/router';

   // ...

   constructor(private route: ActivatedRoute) {
     this.route.params.subscribe(params => {
       const id = params['id'];
       // Use o ID para carregar os dados do produto com esse ID
     });
   }
   ```

3. **Navegação**:
   Para navegar para a página de detalhes do produto, você pode usar um link com um parâmetro `id` específico. Por exemplo, ao clicar em um produto em uma lista, você pode navegar para a página de detalhes do produto com o ID correspondente.

   ```html
   <!-- Lista de produtos -->
   <a [routerLink]="'/produto/' + produto.id">{{ produto.nome }}</a>
   ```

4. **Renderização de Dados**:
   Renderize os detalhes do produto com base nos dados carregados usando o ID fornecido na URL.

   ```html
   <!-- DetalhesProdutoComponent -->
   <h2>Detalhes do Produto</h2>
   <p>ID do Produto: {{ id }}</p>
   <!-- Renderize os detalhes do produto com base no ID -->
   ```

Dessa forma, ao acessar uma URL como `/produto/123`, o Angular direcionará a solicitação para o componente `DetalhesProdutoComponent` e fornecerá o ID 123 como um parâmetro na rota. Você pode usar esse ID para carregar os detalhes do produto correspondente.

As rotas dinâmicas são poderosas para criar páginas de detalhes ou exibição de informações individuais com base em identificadores exclusivos. Certifique-se de definir as rotas apropriadas, acessar os parâmetros da rota no componente e renderizar os detalhes com base nos dados carregados.