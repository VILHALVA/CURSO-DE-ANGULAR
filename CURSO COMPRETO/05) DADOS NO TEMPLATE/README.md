# DADOS NO TEMPLATE
Na linguagem Angular, a interpolação é uma técnica usada para exibir dados das classes dos componentes em um template. Essa é uma das maneiras mais comuns de exibir informações dinâmicas na interface do usuário de um aplicativo Angular. Vou explicar como usar a interpolação:

**1. Configurando Dados no Componente:**
Primeiro, você precisa ter dados em seu componente que deseja exibir no template. Esses dados podem ser propriedades da classe do componente.

Exemplo de componente com algumas propriedades:

```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-meu-componente',
  templateUrl: './meu-componente.component.html',
})
export class MeuComponenteComponent {
  nome: string = 'Alice';
  idade: number = 25;
}
```

**2. Usando Interpolação no Template:**
Agora, você pode exibir esses dados no template usando interpolação. A interpolação é realizada com chaves duplas `{{ }}` no template. Você coloca a expressão que deseja exibir entre as chaves duplas e o Angular a substituirá pelo valor real em tempo de execução.

Exemplo de template usando interpolação:

```html
<p>Nome: {{ nome }}</p>
<p>Idade: {{ idade }}</p>
```

No exemplo acima, `{{ nome }}` e `{{ idade }}` são interpolações que exibirão o valor das propriedades `nome` e `idade` do componente.

**3. Resultado no Navegador:**
Quando o aplicativo é executado no navegador, as interpolações serão substituídas pelos valores reais das propriedades do componente. Portanto, no navegador, você verá algo como:

```
Nome: Alice
Idade: 25
```

As interpolações permitem que você exiba dados dinâmicos de seu componente no template, tornando seu aplicativo Angular interativo e personalizado. Você pode usar interpolações em várias partes do template, como parágrafos, cabeçalhos, listas, atributos HTML e muito mais.