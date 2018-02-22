# Comandos de Base de Dados

Abaixo estão colocados alguns comandos de base de dados da base de dados MongoDB.  
_(Inserir, consultar, atualizar e deletar)_

Para um maior detalhamento sobre cada operação, veja [a referência de cada um deles](#).

---

### `db.{collection-name}.insert({ json })`

Insere na coleção em questão os dados informados no primeiro parâmetro da função `insert()`.

Exemplo de usagem:
```javascript
db.myCollection.insert({ username: "Luiz", name: "Luiz Felipe" });
```

Também aceita arrays com diversos objetos, ao invés de um único objeto.
