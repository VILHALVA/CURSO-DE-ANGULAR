# RENDERIZAÇÃO DE LISTA
A renderização de listas é uma tarefa comum em aplicativos Angular, onde você precisa exibir uma coleção de itens em um formato de lista, como uma lista de tarefas, uma lista de produtos, ou qualquer outra lista de itens. No Angular, você pode usar a diretiva `*ngFor` para renderizar uma lista com base em uma coleção de dados. Eis como você pode fazer isso:

**1. Preparação de Dados:**
   - Primeiro, você precisa ter uma coleção de dados que deseja exibir na lista. Isso pode ser um array de objetos, um array de strings ou qualquer outra coleção de dados.

   Exemplo de uma matriz de strings no componente:
   ```typescript
   listaItens: string[] = ['Item 1', 'Item 2', 'Item 3', 'Item 4'];
   ```

**2. Renderização de Lista no Template:**
   - No seu template, você pode usar a diretiva `*ngFor` para iterar sobre a coleção de dados e renderizar os itens da lista.

   Exemplo de uso da diretiva `*ngFor` no template:
   ```html
   <ul>
     <li *ngFor="let item of listaItens">{{ item }}</li>
   </ul>
   ```

   Neste exemplo, a diretiva `*ngFor` itera sobre `listaItens`, criando um elemento `<li>` para cada item na lista.

**3. Resultado na Interface do Usuário:**
   - Quando o aplicativo é executado no navegador, a lista será renderizada com base nos dados da coleção, exibindo cada item na lista.

   Resultado na interface do usuário:
   ```
   - Item 1
   - Item 2
   - Item 3
   - Item 4
   ```

Você pode personalizar a renderização da lista, adicionar estilos condicionais, vincular eventos aos itens da lista e muito mais. Além disso, a diretiva `*ngFor` oferece flexibilidade para lidar com vários tipos de coleções de dados, como objetos complexos.

A renderização de lista é uma tarefa comum e uma funcionalidade essencial em muitos aplicativos Angular, permitindo que você exiba dados de maneira dinâmica e interativa na interface do usuário.