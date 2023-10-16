# DIRETIVAS DO ANGULAR
As diretivas são recursos poderosos no Angular que permitem estender o HTML com comportamentos personalizados e lógica dinâmica. Elas são usadas para criar componentes reutilizáveis, manipular o DOM, aplicar estilos condicionalmente e muito mais. Existem duas categorias principais de diretivas no Angular:

1. **Diretivas Estruturais**:
   - As diretivas estruturais alteram a estrutura do DOM ao adicionar ou remover elementos HTML com base em condições. As diretivas estruturais mais comuns no Angular são:
     - **`*ngIf`**: Adiciona ou remove elementos com base em uma condição.
     - **`*ngFor`**: Itera sobre uma lista e gera elementos com base nos itens da lista.
     - **`*ngSwitch`**: Controla qual elemento será exibido com base em uma expressão.

   Exemplo de uso do `*ngIf`:
   ```html
   <div *ngIf="mostrarElemento">Este elemento é condicional</div>
   ```

2. **Diretivas de Atributo**:
   - As diretivas de atributo alteram a aparência ou o comportamento de elementos HTML existentes. Elas são aplicadas a elementos HTML usando atributos. Alguns exemplos de diretivas de atributo incluem:
     - **`ngClass`**: Permite adicionar ou remover classes de CSS com base em condições.
     - **`ngStyle`**: Permite definir estilos CSS dinamicamente com base em condições.
     - **`ngModel`**: Usada para criar two-way data binding em campos de formulário.
     - **`ngIf`, `ngFor`, etc. (também podem ser usadas como diretivas de atributo quando não estão em uma sintaxe de estrutura).

   Exemplo de uso do `ngClass`:
   ```html
   <div [ngClass]="{'classe-destaque': destacado, 'classe-padrao': !destacado}">Este elemento tem classes condicionais</div>
   ```

Além das diretivas integradas mencionadas acima, o Angular permite que você crie suas próprias diretivas personalizadas. Diretivas personalizadas são usadas para adicionar comportamentos específicos ao seu aplicativo. Elas podem ser criadas com o Angular CLI ou manualmente.

Para criar uma diretiva personalizada, você pode usar o comando `ng generate directive` do Angular CLI. As diretivas personalizadas são frequentemente usadas para adicionar comportamentos específicos, validação de entrada de usuário, formatação de dados e muito mais.

As diretivas são uma parte fundamental do Angular e desempenham um papel importante na criação de aplicativos ricos em funcionalidades e interatividade. Elas permitem que você crie componentes e elementos de interface de usuário altamente personalizados.