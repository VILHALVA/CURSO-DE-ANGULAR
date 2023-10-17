# PÁGINA DE FORMULÁRIO
A criação de uma página de formulário em um aplicativo Angular é uma tarefa comum. Você pode usar o Angular Forms Module para construir formulários robustos e interativos. Aqui estão os passos para criar uma página de formulário em Angular:

1. **Crie um Componente de Formulário:**

   Use o Angular CLI para gerar um novo componente de formulário. Por exemplo:

   ```bash
   ng generate component formulario
   ```

2. **Defina o Modelo do Formulário:**

   No componente recém-criado, defina o modelo do formulário. Você pode usar o módulo `ReactiveFormsModule` para criar formulários reativos ou o `FormsModule` para criar formulários baseados em modelo. Importe os módulos relevantes em seu módulo.

   ```typescript
   import { ReactiveFormsModule, FormGroup, FormControl, Validators } from '@angular/forms';

   @NgModule({
     imports: [ReactiveFormsModule],
     // ...
   })
   ```

3. **Crie o Formulário:**

   No seu componente, crie um formulário usando o modelo de formulário apropriado (reativo ou baseado em modelo). Por exemplo:

   ```typescript
   formulario: FormGroup;

   constructor() {
     this.formulario = new FormGroup({
       nome: new FormControl('', Validators.required),
       email: new FormControl('', [Validators.required, Validators.email]),
       mensagem: new FormControl(''),
     });
   }
   ```

4. **Vincule o Modelo ao Formulário HTML:**

   No arquivo de modelo HTML do componente, vincule os campos do formulário aos elementos HTML e use a diretiva `formControlName` para fazer a ligação. Por exemplo:

   ```html
   <form [formGroup]="formulario" (submit)="onSubmit()">
     <input type="text" formControlName="nome" placeholder="Nome">
     <input type="email" formControlName="email" placeholder="E-mail">
     <textarea formControlName="mensagem" placeholder="Mensagem"></textarea>
     <button type="submit">Enviar</button>
   </form>
   ```

5. **Trate o Envio do Formulário:**

   Implemente o método `onSubmit()` para lidar com o envio do formulário. Você pode acessar os valores do formulário por meio do modelo do formulário. Por exemplo:

   ```typescript
   onSubmit() {
     if (this.formulario.valid) {
       const values = this.formulario.value;
       // Envie os valores para o servidor ou realize outras ações necessárias.
     }
   }
   ```

6. **Adicione Validação de Formulário:**

   Se desejar adicionar validação personalizada, use os validadores fornecidos pelo Angular ou crie seus próprios validadores personalizados. Você pode exibir mensagens de erro com base nas validações.

7. **Estilize o Formulário:**

   Estilize o formulário e os elementos conforme necessário usando CSS. Você pode adicionar classes, estilos ou usar um pré-processador CSS, como SASS.

8. **Teste e Valide o Formulário:**

   Teste seu formulário para garantir que ele funcione corretamente e que a validação esteja funcionando conforme o esperado.

Isso é um resumo geral de como criar uma página de formulário em um projeto Angular. Lembre-se de que o Angular oferece uma variedade de recursos para lidar com formulários, incluindo validação, rastreamento de alterações e manipulação de erros. Consulte a documentação oficial do Angular sobre formulários para obter informações detalhadas e avançadas sobre como trabalhar com formulários em Angular.