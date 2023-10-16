# RENDERIZAÇÃO CONDICIONAL
A renderização condicional é um conceito importante no desenvolvimento web e é frequentemente usado no Angular para controlar o que é exibido na interface do usuário com base em certas condições. No Angular, você pode realizar a renderização condicional de várias maneiras. Aqui estão alguns cenários comuns e como você pode implementar a renderização condicional:

**1. `*ngIf` Diretiva:**
   - A diretiva `*ngIf` permite que você adicione ou remova elementos do DOM com base em uma condição. Se a condição for verdadeira, o elemento será exibido; caso contrário, ele será removido do DOM.

   Exemplo de uso do `*ngIf`:
   ```html
   <div *ngIf="mostrarElemento">Este elemento é exibido se mostrarElemento for verdadeiro.</div>
   ```

**2. `*ngFor` Diretiva:**
   - A diretiva `*ngFor` é usada para iterar sobre uma coleção, como um array, e renderizar elementos repetidamente com base nos itens da coleção.

   Exemplo de uso do `*ngFor`:
   ```html
   <ul>
     <li *ngFor="let item of listaItens">{{ item }}</li>
   </ul>
   ```

**3. `ngSwitch` Diretiva:**
   - A diretiva `ngSwitch` é usada quando você precisa alternar entre vários elementos com base em uma expressão. Você pode combinar `ngSwitch`, `ngSwitchCase` e `ngSwitchDefault` para criar renderização condicional com várias opções.

   Exemplo de uso do `ngSwitch`:
   ```html
   <div [ngSwitch]="escolha">
     <p *ngSwitchCase="'opcao1'">Opção 1</p>
     <p *ngSwitchCase="'opcao2'">Opção 2</p>
     <p *ngSwitchDefault>Opção padrão</p>
   </div>
   ```

**4. Usando Variáveis Booleanas:**
   - Você pode usar variáveis booleanas no seu componente para controlar a renderização condicional no template. Por exemplo, você pode definir uma variável `mostrarElemento` no componente e usá-la com `*ngIf` no template.

   Exemplo de variável booleana no componente:
   ```typescript
   mostrarElemento: boolean = true;
   ```

   Exemplo de uso no template:
   ```html
   <div *ngIf="mostrarElemento">Este elemento é exibido se mostrarElemento for verdadeiro.</div>
   ```

A renderização condicional é uma técnica essencial para criar interfaces de usuário dinâmicas e interativas em aplicativos Angular. Ela permite que você controle o que é exibido com base em estados, dados e interações do usuário, proporcionando uma experiência mais rica e personalizada para os usuários.