# PIPE OPERATORS DO ANGULAR
Em Angular, os pipe operators são uma parte fundamental do sistema de templates e são usados para transformar dados exibidos no modelo de uma maneira mais conveniente para o usuário. Os pipes permitem formatar, filtrar, classificar e manipular dados antes de serem exibidos na interface do usuário. Aqui estão alguns dos operadores de pipe mais comuns e úteis no Angular:

1. **Operador `{{ expression | currency: 'USD':true:'1.2-2' }}`**:
   - O operador `currency` formata uma expressão numérica como uma moeda. Os argumentos opcionais permitem personalizar o formato, como a moeda (por exemplo, 'USD'), a exibição de símbolo de moeda (booleano) e o número de casas decimais.

2. **Operador `{{ expression | date: 'yyyy-MM-dd' }}`**:
   - O operador `date` formata uma data para um formato específico. Você pode definir o formato desejado passando uma string de formato, como 'yyyy-MM-dd'.

3. **Operador `{{ expression | lowercase }}`**:
   - O operador `lowercase` converte uma string em letras minúsculas.

4. **Operador `{{ expression | uppercase }}`**:
   - O operador `uppercase` converte uma string em letras maiúsculas.

5. **Operador `{{ expression | slice: start:end }}`**:
   - O operador `slice` retorna uma parte de uma string ou um array. Você especifica o índice de início e, opcionalmente, o índice de término.

6. **Operador `{{ expression | number: '1.2-2' }}`**:
   - O operador `number` formata uma expressão numérica com um número específico de casas decimais e separadores de milhar.

7. **Operador `{{ expression | percent }}`**:
   - O operador `percent` formata um número como uma porcentagem.

8. **Operador `{{ expression | async }}`**:
   - O operador `async` é usado para trabalhar com observables. Ele aguarda a resolução de um observable e exibe o valor resultante.

9. **Operador `{{ expression | json }}`**:
   - O operador `json` converte um objeto JavaScript em uma representação de string JSON.

10. **Operador `{{ expression | customPipe: arg1: arg2 }}`**:
    - Você também pode criar seus próprios pipes personalizados. Os pipes personalizados permitem que você defina a lógica de formatação ou filtragem de dados de acordo com suas necessidades específicas.

Além dos operadores mencionados, o Angular fornece uma série de outros pipes internos que podem ser usados para realizar várias transformações de dados nos templates. Os pipes são uma parte poderosa do Angular que simplifica a formatação e a exibição de dados na interface do usuário. Eles tornam o código mais limpo, legível e fácil de manter.