Nos arquivos, que são definidos pelo nome `*.spec.js`, os testes serão realizados.  

# Describe

_**Correntes aplicáveis: `skip`, `only`.**_

_Describes_ geralmente são usados para separar classes distintas e métodos distintos.  
Nesse padrão, poderemos ter um bloco para uma classe _X_ e diversos blocos aninhados referentes a cada método da classe _X_.

Um exemplo de bloco:

```javascript
describe('block name', () => {
  // Test content.
});
```
_**Nota:** Você pode criar blocos aninhados._

# Context

_**Correntes aplicáveis: `skip`, `only`.**_

_Contexts_, semanticamente, são utilizados para definir contextos diferentes em um determinado bloco.  
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

# Correntes

Correntes são métodos que podem vir especificando um comportamento específico para determinado bloco.

## `.only`

Irá executar somente aquele bloco durante o teste.

Por exemplo:
```javascript
describe('main', () => {
  it('should fail', () => {
    throw new Error('just an error');
  });
  
  it.only('should pass', () => {
    // Test will pass here.
  });
});
```

No exemplo acima, nenhum erro ocorrerá, mesmo com a exceção sendo jogada, tendo em vista que o único teste que rodará é o _`'should pass'`_, tendo em vista que colocamos, em corrente, o método `.only`, o que fará com que somente este teste seja executado.
