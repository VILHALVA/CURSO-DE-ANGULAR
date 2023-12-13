# CURSO DE ANGULAR
👨‍⚖️ANGULAR É UM FRAMEWORK DE DESENVOLVIMENTO WEB CRIADO PELO GOOGLE, QUE PERMITE A CRIAÇÃO DE APLICAÇÕES WEB ROBUSTAS E DINÂMICAS USANDO JAVASCRIPT OU TYPESCRIPT. ELE FORNECE UMA ESTRUTURA PARA ORGANIZAR O CÓDIGO, GERENCIAR O ESTADO DA APLICAÇÃO E CRIAR COMPONENTES REUTILIZÁVEIS.

[![GitHub Repo stars](https://img.shields.io/badge/VILHALVA-GITHUB-03A9F4?logo=github)](https://github.com/VILHALVA) 
[![GitHub Repo stars](https://img.shields.io/badge/VEJA%20OS-VIDEOS-03A9F4?logo=youtube)](https://www.youtube.com/@vilhalva100/search?query=Angular) 
[![GitHub Repo stars](https://img.shields.io/badge/VEJA-DOCUMENTAÇÃO-03A9F4?logo=google)](https://angular.io/docs) 
[![GitHub Repo stars](https://img.shields.io/badge/LINGUAGEM%20DE-PROGRAMAÇÃO-03A9F4?logo=github)](https://github.com/VILHALVA/CURSO-DE-JAVASCRIPT)
<br>

[![GitHub Repo stars](https://img.shields.io/badge/-PLAYLIST%20DO%20YOUTUBE-blueviolet)](https://youtube.com/playlist?list=PLnDvRpP8Bnex2GQEN0768_AxZg_RaIGmw&si=1iAmXfOemX42j5ny)

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/cf/Angular_full_color_logo.svg/250px-Angular_full_color_logo.svg.png" align="center" width="280"> <br>

![](https://i.imgur.com/waxVImv.png)

# CONCEITO:
O Angular é um popular framework de desenvolvimento front-end mantido pelo Google, e é amplamente utilizado para criar aplicativos da web robustos e dinâmicos. Aqui estão alguns conceitos-chave, exemplos de código e explicações:

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

Estes são apenas alguns dos conceitos essenciais do Angular. 

# CARACTERISTICAS:
## Características Positivas:

1. **Estrutura Modular e Organização**: O Angular promove uma estrutura organizada e modular para o desenvolvimento de aplicativos. Os módulos, componentes e serviços facilitam a organização do código.

2. **Injeção de Dependência**: O sistema de injeção de dependência do Angular torna o código mais modular e reutilizável, facilitando a manutenção e o teste.

3. **Roteamento Integrado**: O Angular fornece um sistema de roteamento completo que permite criar aplicativos de várias páginas com facilidade.

4. **Tipagem Estática**: O Angular usa o TypeScript, que é um superconjunto do JavaScript com tipagem estática. Isso ajuda a detectar erros de compilação durante o desenvolvimento.

5. **Ferramentas e Ecossistema**: Angular é apoiado pelo Google e tem um ecossistema maduro de ferramentas, bibliotecas e recursos adicionais, como o Angular CLI.

6. **Suporte a Aplicativos Móveis**: O Angular possui o Ionic Framework, que permite o desenvolvimento de aplicativos móveis híbridos usando tecnologias web.

7. **Performance**: O Angular oferece mecanismos eficientes para otimização de desempenho, como detecção de mudanças, carregamento preguiçoso de módulos e AOT (Ahead-of-Time) compilation.

## Características Negativas:

1. **Curva de Aprendizado**: Angular pode ter uma curva de aprendizado mais íngreme, especialmente para iniciantes, devido à complexidade de seus conceitos.

2. **Verbosidade**: O Angular pode parecer mais verboso em comparação com outros frameworks mais leves, o que pode levar a uma quantidade maior de código.

3. **Complexidade**: Para aplicativos simples, o Angular pode ser excessivamente complexo. Ele pode ser uma escolha exagerada para projetos menores.

4. **Tamanho do Pacote**: Os aplicativos Angular podem gerar pacotes maiores em comparação com alguns outros frameworks, o que pode impactar o tempo de carregamento da página.

5. **Dependência de Terceiros**: O Angular inclui muitas funcionalidades internas, o que pode aumentar o tamanho do pacote e a dependência de terceiros.

6. **Migração entre Versões**: Migrações entre diferentes versões do Angular podem ser desafiadoras, especialmente quando mudanças significativas são introduzidas.

7. **Dificuldade de SEO**: O Angular é um framework baseado em JavaScript, o que pode tornar o SEO (otimização para mecanismos de busca) mais desafiador em comparação com aplicativos mais tradicionais.

## TRABALHANDO COM ANGULAR:
Trabalhar com o Angular é relativamente simples, especialmente quando se utiliza o Angular CLI, que automatiza muitas tarefas. Aqui está uma explicação simplificada:

**1. Instalação Inicial:**
   - Inicialmente, você precisa ter o Node.js instalado em seu sistema.
   - Em seguida, você instala o Angular CLI globalmente com o comando `npm install -g @angular/cli`. Isso permite que você crie e gerencie projetos Angular em qualquer lugar.

**2. Criar um Novo Projeto:**
   - Usando o Angular CLI, você pode criar um novo projeto Angular com um único comando, como `ng new nome-do-seu-projeto`.
   - O Angular CLI cuida de configurar toda a estrutura do projeto para você.

**3. Estrutura do Projeto:**
   - A maior parte do trabalho acontece na pasta `src/app`. Aqui estão os principais pontos:

      - **src/app/app.component.ts:** Este é o arquivo que define o componente raiz do aplicativo.
      - **src/app/app.component.html:** Aqui você define o template HTML do componente raiz.
      - **src/app/app.component.css (opcional):** Pode conter estilos CSS específicos do componente raiz.

**4. Componentes e Módulos:**
   - Você pode criar componentes adicionais usando o comando `ng generate component nome-do-seu-componente`.
   - Os componentes são organizados em subpastas dentro de `src/app`.
   - Você pode criar módulos para agrupar componentes relacionados usando o comando `ng generate module nome-do-seu-modulo`.

**5. Servidor de Desenvolvimento:**
   - Você inicia o servidor de desenvolvimento com o comando `ng serve`. Isso permite que você veja o aplicativo em execução em `http://localhost:4200` e atualizações em tempo real enquanto você faz alterações no código.

**6. Personalização:**
   - Você pode personalizar os componentes e modelos em `src/app` para criar a interface do usuário desejada.
   - Pode adicionar serviços e outros recursos conforme necessário para implementar a lógica de negócios do aplicativo.

**7. Teste e Implantação:**
   - O Angular CLI oferece comandos para criar testes e construir o aplicativo para implantação.

Resumindo, o Angular CLI simplifica muito o processo de desenvolvimento Angular, e a maior parte do trabalho acontece dentro da pasta `src/app`. A estrutura organizada, os comandos simplificados e o servidor de desenvolvimento facilitam a criação de aplicativos web dinâmicos com Angular. Além disso, o Angular oferece uma ampla variedade de recursos e bibliotecas para facilitar o desenvolvimento de aplicativos robustos.
