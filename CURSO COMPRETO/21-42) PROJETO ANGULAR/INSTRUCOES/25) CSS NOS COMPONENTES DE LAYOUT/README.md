# CSS NOS COMPONENTES DE LAYOUT
No Angular, você pode estilizar os componentes de layout usando CSS de várias maneiras. Aqui estão algumas opções comuns para aplicar estilos a componentes de layout:

1. **Estilos CSS Internos:** Você pode definir estilos CSS diretamente no arquivo `.component.css` associado a um componente específico. Isso é útil quando você deseja aplicar estilos exclusivos a um componente específico. Por exemplo:

```css
/* styles.component.css */
.container {
  background-color: #f0f0f0;
  padding: 10px;
}
```

E no arquivo `.component.ts`:

```typescript
@Component({
  selector: 'app-layout',
  templateUrl: './layout.component.html',
  styleUrls: ['./layout.component.css']
})
```

2. **Estilos CSS Externos:** Você pode criar um arquivo CSS externo e vinculá-lo ao componente usando o atributo `styleUrls`. Isso é útil quando você deseja manter estilos separados em arquivos diferentes. Por exemplo:

```css
/* layout-styles.css */
.container {
  background-color: #f0f0f0;
  padding: 10px;
}
```

```typescript
@Component({
  selector: 'app-layout',
  templateUrl: './layout.component.html',
  styleUrls: ['./layout-styles.css']
})
```

3. **Estilos Inline:** Você também pode aplicar estilos diretamente nos elementos HTML usando o atributo `style`. No entanto, isso é mais útil para pequenos ajustes de estilo.

```html
<div style="background-color: #f0f0f0; padding: 10px;">
  Conteúdo do componente de layout
</div>
```

4. **Estilos de Terceiros:** Se você estiver usando bibliotecas ou frameworks de terceiros, siga as instruções fornecidas pela documentação da biblioteca para aplicar estilos.

5. **Pré-processadores CSS:** Você também pode optar por usar pré-processadores CSS, como SASS ou LESS, para escrever estilos mais avançados. O Angular suporta essas tecnologias de pré-processamento de CSS.

Lembre-se de que a aplicação de estilos no Angular segue os princípios do CSS, como seletores, classes, IDs e herança. Você pode usar seletores CSS para segmentar elementos específicos dentro do componente de layout e estilizá-los de acordo com as necessidades do seu projeto. Certifique-se de seguir as práticas recomendadas de estilização CSS para manter seu código organizado e legível.