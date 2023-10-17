# CSS PÁGINA DE MOMENTOS
Para estilizar uma página de momentos em um aplicativo Angular, você pode criar um arquivo CSS (cascading style sheet) dedicado ao estilo da página. Vou fornecer um exemplo de CSS que você pode usar como ponto de partida para a sua página de momentos. Lembre-se de personalizar o estilo de acordo com as diretrizes de design do seu aplicativo. Aqui está um exemplo de CSS para a página de momentos:

```css
/* Estilização da página de momentos */

/* Estilos para o contêiner principal da página */
.momentos-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
}

/* Estilos para os cartões de momentos */
.momento-card {
  width: 300px;
  border: 1px solid #e0e0e0;
  margin: 10px;
  padding: 10px;
  border-radius: 5px;
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  transition: transform 0.2s;
}

.momento-card:hover {
  transform: scale(1.03);
}

/* Estilos para a imagem do momento */
.momento-img {
  max-width: 100%;
  height: auto;
}

/* Estilos para o título do momento */
.momento-titulo {
  font-size: 1.2rem;
  font-weight: bold;
  margin-top: 10px;
}

/* Estilos para a descrição do momento */
.momento-descricao {
  font-size: 0.9rem;
  color: #555;
}

/* Estilos para o botão "Ver Detalhes" */
.momento-link {
  display: block;
  text-align: center;
  background-color: #007bff;
  color: #fff;
  padding: 8px 16px;
  margin-top: 10px;
  text-decoration: none;
  border-radius: 4px;
}

.momento-link:hover {
  background-color: #0056b3;
}
```

Neste exemplo de CSS, estamos estilizando os cartões de momentos e definindo estilos para a imagem, título, descrição e um botão "Ver Detalhes" que pode direcionar os usuários para a página individual de um momento.

Você pode vincular essas classes CSS aos elementos correspondentes no modelo HTML do componente de momentos. Por exemplo:

```html
<!-- momento.component.html -->
<div class="momentos-container">
  <div class="momento-card" *ngFor="let momento of momentos">
    <img class="momento-img" [src]="momento.imagem" alt="Imagem do Momento" />
    <h2 class="momento-titulo">{{ momento.titulo }}</h2>
    <p class="momento-descricao">{{ momento.descricao }}</p>
    <a class="momento-link" [routerLink]="['/momento', momento.id]">Ver Detalhes</a>
  </div>
</div>
```

Certifique-se de que as classes CSS no seu arquivo `.css` correspondam às classes usadas no seu modelo HTML. Isso garantirá que os estilos sejam aplicados adequadamente.

Lembre-se de que o exemplo acima é apenas um ponto de partida. Você pode personalizar os estilos, as cores e as fontes de acordo com as diretrizes de design do seu aplicativo. Além disso, considere a responsividade e a experiência do usuário ao estilizar a página de momentos para garantir que ela seja visualmente agradável e funcional em dispositivos de diferentes tamanhos.