# TWO WAY DATA BINDING NO ANGULAR
O two-way data binding (ligação de dados bidirecional) é uma funcionalidade fundamental do Angular que permite a sincronização de dados entre o modelo (componente) e a visão (template) em ambas as direções. Isso significa que as alterações no modelo são refletidas automaticamente na visão e vice-versa. No Angular, você pode alcançar o two-way data binding usando a diretiva `ngModel`.

Aqui está um exemplo de como usar o two-way data binding no Angular:

1. **Importe o Módulo `FormsModule`**:
   Certifique-se de importar o módulo `FormsModule` no seu módulo principal (geralmente `app.module.ts`) para usar a funcionalidade de two-way data binding. Isso é necessário porque o two-way data binding depende da diretiva `ngModel`.

   ```typescript
   import { FormsModule } from '@angular/forms';

   @NgModule({
     imports: [FormsModule],
     // ...
   })
   export class AppModule { }
   ```

2. **No Template (HTML)**:
   No seu template, você pode usar a diretiva `ngModel` para criar uma ligação bidirecional entre um elemento HTML, como um campo de entrada (input), e uma propriedade no seu componente. Aqui está um exemplo com um campo de entrada:

   ```html
   <input [(ngModel)]="nome" placeholder="Seu nome">
   <p>Olá, {{ nome }}!</p>
   ```

   Neste exemplo, `[(ngModel)]="nome"` estabelece uma ligação bidirecional entre o valor do campo de entrada e a propriedade `nome` no componente.

3. **No Componente (TypeScript)**:
   No componente correspondente, você deve declarar a propriedade `nome` e inicializá-la. O Angular cuidará da sincronização entre o campo de entrada e a propriedade.

   ```typescript
   import { Component } from '@angular/core';

   @Component({
     selector: 'app-meu-componente',
     template: `
       <input [(ngModel)]="nome" placeholder="Seu nome">
       <p>Olá, {{ nome }}!</p>
     `
   })
   export class MeuComponenteComponent {
     nome: string = 'Mundo';
   }
   ```

Com essa configuração, qualquer alteração no campo de entrada será refletida automaticamente na propriedade `nome` do componente, e qualquer alteração na propriedade `nome` no componente também será refletida no campo de entrada e na exibição.

O two-way data binding é uma característica poderosa do Angular que simplifica a comunicação entre a visão e o modelo, economizando tempo e reduzindo a necessidade de manipulação manual dos dados. É especialmente útil para formulários e interações de entrada do usuário. Certifique-se de importar o módulo `FormsModule` e usar a diretiva `ngModel` para aproveitar essa funcionalidade.