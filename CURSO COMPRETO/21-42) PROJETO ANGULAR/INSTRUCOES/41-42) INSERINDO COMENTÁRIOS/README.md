# INSERINDO COMENTÁRIOS
Para inserir comentários em um aplicativo Angular após a criação do formulário de comentários, siga os passos abaixo:

**Passo 1: Lógica de Inserção de Comentários:**

Dentro do método `enviarComentario()` no componente `FormularioComentarios`, implemente a lógica para enviar o comentário para o servidor ou para o local onde você deseja armazenar os comentários. Geralmente, isso envolve a chamada a um serviço para enviar o comentário.

```typescript
// formulario-comentarios.component.ts
import { Component } from '@angular/core';
import { FormBuilder, FormGroup, Validators } from '@angular/forms';
import { ComentariosService } from './comentarios.service'; // Importe o serviço de comentários

@Component({
  selector: 'app-formulario-comentarios',
  templateUrl: './formulario-comentarios.component.html',
})
export class FormularioComentariosComponent {
  formulario: FormGroup;

  constructor(private fb: FormBuilder, private comentariosService: ComentariosService) {
    this.formulario = this.fb.group({
      comentario: ['', [Validators.required]],
    });
  }

  enviarComentario() {
    if (this.formulario.valid) {
      const comentario = this.formulario.get('comentario').value;
      // Chame o serviço para enviar o comentário
      this.comentariosService.inserirComentario(comentario).subscribe(() => {
        // O comentário foi inserido com sucesso, você pode atualizar a lista de comentários ou tomar outras ações necessárias
      });
    }
  }
}
```

**Passo 2: Serviço de Comentários:**

Crie um serviço de comentários (por exemplo, `ComentariosService`) que contenha a lógica para enviar o comentário ao servidor ou armazená-lo no banco de dados local. Este serviço será injetado no componente de formulário de comentários.

```typescript
// comentarios.service.ts
import { Injectable } from '@angular/core';
import { HttpClient } from '@angular/common/http';
import { Observable } from 'rxjs';

@Injectable({
  providedIn: 'root',
})
export class ComentariosService {
  private apiUrl = 'https://sua-api.com/comentarios'; // Substitua pelo URL da sua API de comentários

  constructor(private http: HttpClient) {}

  inserirComentario(comentario: string): Observable<any> {
    // Implemente a lógica para enviar o comentário para o servidor
    return this.http.post(this.apiUrl, { comentario });
  }
}
```

**Passo 3: Atualização da Lista de Comentários (Opcional):**

Depois de inserir um comentário com sucesso, você pode atualizar a lista de comentários para exibir o novo comentário imediatamente. Para fazer isso, chame o serviço que recupera a lista de comentários e atualize a interface do usuário.

**Passo 4: Teste:**

Teste a inserção de comentários para garantir que os comentários sejam enviados corretamente e que a interface do usuário seja atualizada conforme necessário.

**Passo 5: Lidar com Erros:**

Certifique-se de lidar com erros que possam ocorrer durante a inserção de comentários, como falhas na solicitação HTTP ou erros no servidor. Forneça feedback adequado ao usuário em caso de erro.

**Passo 6: Documentação:**

Documente a funcionalidade de inserção de comentários, incluindo como ela funciona e quaisquer detalhes importantes relacionados aos comentários no seu aplicativo.

Personalize a implementação de acordo com os requisitos específicos do seu aplicativo e considere a segurança e as permissões adequadas para garantir que apenas os usuários autorizados possam inserir comentários.