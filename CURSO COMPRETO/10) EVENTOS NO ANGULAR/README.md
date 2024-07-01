# EVENTOS NO ANGULAR
No Angular, os eventos são interações do usuário ou ações que desencadeiam respostas específicas no aplicativo. Você pode capturar e responder a eventos em componentes Angular de várias maneiras. Aqui estão alguns conceitos-chave relacionados a eventos no Angular:

1. **Event Binding (Vinculação de Eventos)**:
   - O Angular permite que você associe eventos HTML, como cliques, teclas pressionadas, foco e muito mais, a métodos em seu componente. Isso é chamado de "event binding." Você vincula um evento HTML a um método no componente usando parênteses `()`. Quando o evento ocorre, o método correspondente é chamado.

   Exemplo de event binding:
   ```html
   <button (click)="onButtonClick()">Clique em mim</button>
   ```

   No componente, você implementa o método `onButtonClick` para responder ao evento de clique:
   ```typescript
   onButtonClick() {
     // Lógica a ser executada quando o botão é clicado.
   }
   ```

2. **$event Object**:
   - Ao capturar eventos, você pode acessar o objeto `$event`, que contém informações sobre o evento, como dados de formulários, coordenadas de clique e muito mais. O `$event` é passado automaticamente para o método do componente vinculado ao evento.

   Exemplo de uso do `$event` em um evento de clique:
   ```html
   <button (click)="onButtonClick($event)">Clique em mim</button>
   ```

   No componente, você pode acessar as propriedades do evento, como `event.target` ou `event.clientX`, conforme necessário.

3. **Event Emitter (Emissor de Eventos)**:
   - Em alguns casos, você pode precisar criar eventos personalizados para permitir a comunicação entre componentes. Isso é feito usando o `EventEmitter` do Angular. Você declara um emissor de evento em um componente e pode emitir eventos personalizados usando o método `emit` do emissor.

   Exemplo de declaração de emissor de evento no componente:
   ```typescript
   @Output() meuEvento = new EventEmitter<string>();
   ```

   Exemplo de emissão de evento personalizado no componente:
   ```typescript
   this.meuEvento.emit("Dados do evento");
   ```

   No template, você pode vincular esse evento personalizado a um método em outro componente para responder ao evento.

4. **Diretivas de Evento**:
   - O Angular fornece diretivas de evento integradas, como `(click)`, `(keydown)`, `(focus)`, etc., que permitem vincular eventos diretamente em elementos HTML em seu template.

   Exemplo de uso da diretiva de evento `(click)`:
   ```html
   <button (click)="onButtonClick()">Clique em mim</button>
   ```

   Você também pode usar diretivas de evento personalizadas, caso crie diretivas personalizadas para lidar com eventos específicos.

Os eventos desempenham um papel fundamental na criação de aplicativos interativos em Angular, permitindo que você capture ações do usuário, comunique-se entre componentes e responda dinamicamente às interações na interface do usuário.