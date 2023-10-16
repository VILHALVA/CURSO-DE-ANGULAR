# EMITINDO EVENTOS
No Angular, você pode emitir eventos personalizados de um componente para notificar outros componentes ou partes do aplicativo sobre a ocorrência de algum evento específico. Para emitir eventos personalizados, você pode usar o Angular's `EventEmitter`. Aqui está como você pode emitir eventos personalizados:

**1. Declaração de um Event Emitter:**
   - No componente onde você deseja emitir um evento, primeiro declare uma instância de `EventEmitter` como uma propriedade do componente. Você deve importar `EventEmitter` de `@angular/core`.

   Exemplo de declaração de um emissor de evento no componente:
   ```typescript
   import { Component, EventEmitter, Output } from '@angular/core';

   @Component({
     selector: 'app-meu-componente',
     template: '<button (click)="emitirEvento()">Emitir Evento</button>',
   })
   export class MeuComponenteComponent {
     @Output() meuEvento = new EventEmitter<string>();

     emitirEvento() {
       this.meuEvento.emit('Dados do evento personalizado');
     }
   }
   ```

**2. Uso no Template:**
   - No exemplo acima, usamos `(click)="emitirEvento()"` para associar o evento de clique do botão ao método `emitirEvento()` que, por sua vez, emite o evento personalizado.

**3. Recepção em Outro Componente:**
   - Para receber e reagir ao evento personalizado em outro componente, você deve adicionar o seletor do componente que emite o evento ao template do componente receptor e vincular o evento usando a sintaxe de vinculação de eventos.

   Exemplo de uso do evento personalizado em outro componente:
   ```html
   <app-meu-componente (meuEvento)="lidarComEvento($event)"></app-meu-componente>
   ```

   No código acima, `(meuEvento)="lidarComEvento($event)"` vincula o evento personalizado `meuEvento` do componente `app-meu-componente` ao método `lidarComEvento($event)` do componente receptor.

**4. Lidar com o Evento no Componente Receptor:**
   - No componente receptor, você deve implementar o método `lidarComEvento` para tratar os dados do evento emitido. O argumento `$event` conterá os dados emitidos com o evento.

   Exemplo de método para lidar com o evento no componente receptor:
   ```typescript
   lidarComEvento(dadosEvento: string) {
     // Lógica para lidar com o evento personalizado
     console.log('Evento emitido com dados:', dadosEvento);
   }
   ```

Dessa forma, você pode emitir eventos personalizados de um componente e reagir a esses eventos em outros componentes. Isso é útil para permitir a comunicação entre componentes em diferentes partes do seu aplicativo Angular. Certifique-se de que os componentes envolvidos tenham uma relação pai-filho ou que estejam de alguma forma conectados no aplicativo.