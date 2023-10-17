# INICIANDO COMPONENTE DE MENSAGEM
Para criar um componente de mensagem em um aplicativo Angular, você pode seguir os passos abaixo. Neste exemplo, vamos criar um componente simples de mensagem que permite exibir mensagens na interface do usuário.

**Passo 1: Crie um novo componente de mensagem**

Use o Angular CLI para criar um novo componente de mensagem. No seu terminal, execute o seguinte comando:

```bash
ng generate component mensagem
```

Isso criará a estrutura de arquivos para o componente de mensagem, incluindo arquivos de modelo, estilo e classe de componente.

**Passo 2: Defina o Modelo do Componente de Mensagem**

No arquivo HTML do componente `mensagem`, você pode definir o modelo para a exibição da mensagem. Por exemplo:

```html
<!-- mensagem.component.html -->
<div class="mensagem" *ngIf="mensagem">
  <p>{{ mensagem }}</p>
</div>
```

**Passo 3: Estilize o Componente de Mensagem**

Você pode estilizar o componente de mensagem definindo estilos no arquivo CSS do componente. Aqui está um exemplo simples de estilos:

```css
/* mensagem.component.css */
.mensagem {
  background-color: #dff0d8;
  border: 1px solid #3c763d;
  color: #3c763d;
  padding: 10px;
  margin: 10px 0;
  border-radius: 4px;
}
```

**Passo 4: Defina a Lógica de Exibição da Mensagem no Componente**

No arquivo de classe do componente `mensagem`, você pode definir a lógica para exibir e ocultar a mensagem. Aqui, usaremos uma variável `mensagem` que será atualizada para exibir a mensagem no modelo quando necessário:

```typescript
// mensagem.component.ts
import { Component, Input } from '@angular/core';

@Component({
  selector: 'app-mensagem',
  templateUrl: './mensagem.component.html',
  styleUrls: ['./mensagem.component.css']
})
export class MensagemComponent {
  @Input() mensagem: string | null = null;
}
```

Neste exemplo, usamos a diretiva `@Input` para permitir que a mensagem seja passada para o componente de fora.

**Passo 5: Use o Componente de Mensagem em Outros Componentes**

Agora você pode usar o componente de mensagem em outros componentes quando desejar exibir uma mensagem para o usuário. Por exemplo, em um componente pai, você pode fazer algo como:

```html
<!-- componente-pai.component.html -->
<app-mensagem [mensagem]="mensagemParaExibir"></app-mensagem>
```

E no arquivo de classe do componente pai, você pode definir `mensagemParaExibir` com a mensagem que deseja mostrar no componente de mensagem.

Isso é um exemplo básico de como criar um componente de mensagem em um aplicativo Angular. Você pode personalizá-lo e aprimorá-lo conforme necessário, adicionando recursos como animações, temporizadores de expiração para mensagens e estilização mais avançada.