# CSS NO ANGULAR
O CSS desempenha um papel fundamental na criação de interfaces de usuário atraentes e estilizadas em aplicativos Angular. O Angular permite que você aplique estilos CSS de várias maneiras. Aqui estão as principais abordagens para trabalhar com CSS em projetos Angular:

1. **Estilos Globais**: Você pode adicionar estilos globais a um projeto Angular editando o arquivo `styles.css` na pasta `src` do seu projeto. Os estilos definidos nesse arquivo serão aplicados a todas as partes do seu aplicativo.

2. **Estilos de Componente**: Para criar estilos específicos para um componente, você pode criar um arquivo CSS (por exemplo, `seu-componente.component.css`) no mesmo diretório onde o componente está localizado. Os estilos definidos nesse arquivo afetarão apenas o componente correspondente.

   Exemplo de arquivo CSS de componente:
   ```css
   /* seu-componente.component.css */
   .classe-do-seu-componente {
     color: blue;
   }
   ```

   Você pode usar essas classes em seu template para estilizar os elementos HTML específicos do seu componente.

3. **Estilos Inline**: Além de usar classes definidas em arquivos CSS de componente, você também pode aplicar estilos diretamente a elementos HTML usando a propriedade `style` do Angular.

   Exemplo de uso de estilo inline no template:
   ```html
   <div [style.color]="corDoTexto">Texto com cor dinâmica</div>
   ```

   No componente, você definiria a propriedade `corDoTexto` com um valor dinâmico.

4. **Estilos Condicionais**: Você pode aplicar estilos com base em condições ou expressões diretamente no template usando a diretiva `ngStyle` ou `ngClass`.

   Exemplo de uso de `ngStyle` no template:
   ```html
   <div [ngStyle]="{ 'font-weight': negrito ? 'bold' : 'normal' }">Texto em negrito</div>
   ```

   Exemplo de uso de `ngClass` no template:
   ```html
   <div [ngClass]="{'destacado': destacarElemento, 'sublinhado': sublinharElemento}">Texto com classes condicionais</div>
   ```

5. **Pré-processadores CSS**: Se você preferir usar pré-processadores CSS, como Sass ou Less, o Angular oferece suporte a eles. Você pode criar arquivos `.scss` ou `.less` em vez de `.css`, e o Angular irá compilar esses arquivos para CSS durante o processo de construção.

Lembre-se de que, ao usar o Angular, é uma boa prática manter seu código CSS organizado e bem estruturado para facilitar a manutenção e evitar conflitos de estilos. O encapsulamento de estilos é um recurso fundamental do Angular, que ajuda a evitar que estilos de um componente afetem outros componentes inadvertidamente.

Experimente as diferentes abordagens de estilização em seu projeto Angular e escolha a que melhor atenda às necessidades de design e organização do seu aplicativo.