Nos arquivos, que são definidos pelo nome `*.spec.js`, os testes serão realizados.  

# Blocos

_**Correntes aplicáveis: `skip`, `only`.**_

Blocos geralmente são usados para separar classes distintas e métodos distintos.  
Nesse padrão, poderemos ter um bloco para uma classe _X_ e diversos blocos aninhados referentes a cada método da classe _X_.

Um exemplo de bloco:

```javascript
describe('block name', () => {
  // Test content.
});
```
_**Nota:** Você pode criar blocos aninhados._

# Contextos

_**Correntes aplicáveis: `skip`, `only`.**_

Contextos, semanticamente, são utilizados para definir contextos diferentes em um determinado bloco.  
Geralmente são utilizados para definir ações diferentes que podem ser tomadas dentro de um bloco dado o seu contexto de execução (por exemplo, um parâmetro que definirá a ação a ser tomada, etc).

Exemplo:
```javascript
describe('block name', () => {
  context('context name', () => {
    // Context content.
  });
});
```

# It

_**Correntes aplicáveis: `skip`, `only`.**_

`It` é o teste individual. Cada teste é executado por um `it`.

Exemplo:
```javascript
describe('block name', () => {
  it('should pass', () => {
    // Test will pass here.
  });
});
```

___Nota:__ Se uma exceção for jogada dentro do `it`, o teste não passará._
