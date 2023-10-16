# ANGULAR ROUTER
O Angular Router é uma parte fundamental do framework Angular que permite navegar entre diferentes partes do seu aplicativo web. Ele fornece funcionalidades de roteamento para criar URLs, vincular URLs a componentes específicos e lidar com a navegação do usuário em um aplicativo de página única (SPA). O Angular Router é altamente configurável e permite que você crie aplicativos com várias rotas e exiba diferentes componentes com base nas URLs.

Aqui estão os principais conceitos e recursos relacionados ao Angular Router:

1. **Configuração de Rotas**:
   - Você pode configurar rotas no Angular definindo as rotas e os componentes correspondentes em um arquivo de configuração, geralmente no módulo raiz do aplicativo (app.module.ts).

   Exemplo de configuração de rotas:
   ```typescript
   const routes: Routes = [
     { path: '', component: HomeComponent },
     { path: 'about', component: AboutComponent },
     { path: 'products', component: ProductsComponent },
   ];
   ```

2. **Outlet de Roteamento**:
   - Para exibir componentes específicos em um aplicativo Angular, você utiliza um `<router-outlet></router-outlet>` em seu template. O componente correspondente à rota atual será renderizado nesse local.

   Exemplo de utilização do `<router-outlet>` no template:
   ```html
   <router-outlet></router-outlet>
   ```

3. **Navegação**:
   - Para navegar entre as rotas, você pode usar links ancorados em elementos `<a>`, com a diretiva `[routerLink]`, ou pode navegar programaticamente no código TypeScript com a classe `Router`.

   Exemplo de navegação usando `[routerLink]`:
   ```html
   <a routerLink="/about">Sobre nós</a>
   ```

   Exemplo de navegação programática em TypeScript:
   ```typescript
   import { Router } from '@angular/router';

   // ...

   // Navegar para a rota '/about'
   this.router.navigate(['/about']);
   ```

4. **Parâmetros de Rota**:
   - Você pode passar parâmetros nas URLs das rotas, tornando-as dinâmicas. Os parâmetros podem ser recuperados no componente associado à rota.

   Exemplo de rota com parâmetros:
   ```typescript
   { path: 'product/:id', component: ProductDetailComponent }
   ```

5. **Guardas de Rotas**:
   - As guardas de rotas permitem proteger rotas, verificando condições antes de permitir que o usuário acesse uma rota específica. Isso é útil para autenticação, autorização e verificação de dados.

6. **Lazy Loading**:
   - O Angular Router suporta o carregamento preguiçoso (lazy loading), o que significa que os módulos e componentes só são carregados quando o usuário acessa uma rota específica. Isso melhora o desempenho, especialmente em aplicativos maiores.

7. **Roteamento Aninhado**:
   - Você pode aninhar rotas dentro de outras rotas para criar hierarquias de rotas. Isso é útil para criar layouts de aplicativos complexos.

8. **Acesso a Rota Ativa**:
   - O Angular Router fornece informações sobre a rota ativa, como o fragmento da URL, os parâmetros, a consulta, entre outros. Você pode acessar essas informações usando a classe `ActivatedRoute`.

O Angular Router é uma parte essencial do desenvolvimento de aplicativos Angular e permite que você crie aplicativos de página única poderosos e ricos em recursos. Ele fornece um mecanismo de navegação flexível e eficiente, além de facilitar a organização de código em aplicativos maiores. É uma ferramenta poderosa para criar experiências de usuário dinâmicas e interativas.