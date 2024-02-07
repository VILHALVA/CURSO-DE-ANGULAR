# SINTAXE:
## CRIANDO PROJETO:
Criar um projeto Angular é um processo relativamente simples. Aqui está um guia passo a passo para ajudá-lo a começar:

### Passo 1: Instalar o Angular CLI (Command Line Interface)
Certifique-se de ter o Angular CLI instalado globalmente em sua máquina. Você pode instalar usando o npm (Node Package Manager) através do seguinte comando:

```
npm install -g @angular/cli
```

### Passo 2: Criar um novo projeto Angular
Depois de instalar o Angular CLI, você pode criar um novo projeto Angular executando o seguinte comando no terminal:

```
ng new nome-do-projeto
```

Substitua "nome-do-projeto" pelo nome que você deseja dar ao seu projeto.

### Passo 3: Navegar para o diretório do projeto
Após a criação do projeto, navegue até o diretório do projeto usando o comando `cd`:

```
cd nome-do-projeto
```

### Passo 4: Executar o projeto
Depois de estar no diretório do seu projeto, você pode iniciar o servidor de desenvolvimento executando:

```
ng serve
```

Isso iniciará um servidor de desenvolvimento e seu aplicativo estará acessível em `http://localhost:4200/` por padrão.

### Passo 5: Visualizar o projeto
Abra seu navegador da web e vá para `http://localhost:4200/` para visualizar seu novo aplicativo Angular.

### Passo 6: Começar a desenvolver
Agora você pode começar a desenvolver seu projeto Angular. O Angular CLI já gerou a estrutura básica do projeto para você. Você pode adicionar componentes, serviços, módulos e muito mais conforme necessário para o seu aplicativo.

## EXEMPLOS DE CÓDIGOS:
1. **Módulos (Modules)**:
   - Conceito: Os módulos são os blocos de construção fundamentais de um aplicativo Angular. Eles são usados para organizar e dividir a aplicação em partes funcionais.
   - Exemplo de código:
     ```typescript
     import { NgModule } from '@angular/core';

     @NgModule({
       declarations: [AppComponent, HomeComponent],
       imports: [RouterModule, HttpClientModule],
       bootstrap: [AppComponent],
     })
     export class AppModule { }
     ```
   - Explicação: Neste exemplo, um módulo chamado `AppModule` é criado. Ele declara componentes como `AppComponent` e `HomeComponent`, importa outros módulos, como `RouterModule` e `HttpClientModule`, e define o componente de inicialização como `AppComponent`.

2. **Componentes (Components)**:
   - Conceito: Os componentes são partes reutilizáveis e autônomas de uma aplicação Angular. Eles consistem em um HTML, uma classe TypeScript e um arquivo de estilo.
   - Exemplo de código:
     ```typescript
     import { Component } from '@angular/core';

     @Component({
       selector: 'app-root',
       templateUrl: 'app.component.html',
       styleUrls: ['app.component.css']
     })
     export class AppComponent {
       title = 'Meu Aplicativo Angular';
     }
     ```
   - Explicação: Aqui, um componente `AppComponent` é definido. Ele tem um seletor (nome da tag HTML) e associa um template HTML e estilos.

3. **Diretivas (Directives)**:
   - Conceito: As diretivas são instruções no DOM que dizem ao Angular como modificar ou manipular o DOM.
   - Exemplo de código:
     ```html
     <div *ngIf="mostrarMensagem">Esta é uma mensagem condicional.</div>
     ```
   - Explicação: A diretiva `*ngIf` é usada para condicionalmente adicionar ou remover o elemento DOM com base na expressão `mostrarMensagem`.

4. **Injeção de Dependência (Dependency Injection)**:
   - Conceito: O Angular fornece um sistema de injeção de dependência que permite que os componentes obtenham as dependências de que precisam.
   - Exemplo de código:
     ```typescript
     import { Injectable } from '@angular/core';

     @Injectable()
     export class DataService {
       getData() {
         return 'Dados do serviço';
       }
     }
     ```
   - Explicação: Aqui, um serviço chamado `DataService` é criado e marcado como injetável. Ele pode ser injetado em componentes para fornecer funcionalidade de busca de dados.

5. **Roteamento (Routing)**:
   - Conceito: O roteamento permite a navegação entre diferentes componentes em um aplicativo Angular com URLs amigáveis.
   - Exemplo de código (configuração de roteamento):
     ```typescript
     const routes: Routes = [
       { path: '', component: HomeComponent },
       { path: 'about', component: AboutComponent },
     ];
     ```
   - Explicação: Isso configura rotas para as páginas principal e "sobre" do aplicativo.