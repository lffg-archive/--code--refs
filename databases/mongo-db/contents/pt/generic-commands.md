# Comandos Genéricos

Abaixo estão colocados alguns comandos genéricos da base de dados MongoDB.

---

### `show dbs`

Mostra todas as base de dados<sup>[1]</sup> disponíveis, que são seguidas pelo seu espaço no disco.  
Usagem:
```shell
show dbs
```

---

### `use {db-name}` <sup>[2]</sup>

Alterna o contexto para aquela base de dados<sup>[1]</sup> em específico.  
Caso a base de dados especificada não exista, ela será criada.

Exemplo de usagem:
```shell
use database_name_example

# No caso acima, não existe nenhuma base de dados com o nome `database_name_example`,
# logo, ela foi criada; e o contexto do terminal foi alterado para aquela base de dados.
#
# Caso já existisse, nenhuma outra base seria criada, apenas o contexto seria alterado.
```

---

### `db.dropDatabase()`

Remove a base de dados (em contexto), que fora especificada usando o comando `use`<sup>[2]</sup> (acima).

Exemplo de usagem:  
```shell
# Usaremos como contexto a base de dados `school`:
use school

# Remover a base de dados `students`:
db.dropDatabase()
```

---

### `db.createCollection("{collection-name}")`

Cria uma coleção na base de dados (em contexto), que fora especificada usando o comando `use`<sup>[2]</sup> (acima).  
O nome da coleção é especificado substituindo `{collection-name}`.

Exemplo de usagem:  
```shell
# Usaremos como contexto a base de dados `school`:
use school

# Criaremos uma coleção `students`:
db.createCollection("students")
```

---

### `db.getCollectionNames()`

Retorna as coleções da base de dados (em contexto) (em formato de **array**), que fora especificada usando o comando `use`<sup>[2]</sup> (acima).

Exemplo de usagem:
```shell
# Usaremos como contexto a base de dados `school`:
use school

# Criaremos uma coleção `students`:
db.createCollection("students")

# Retornar todas as coleções da base de dados `school`:
db.getCollectionNames()

# Irá retornar:
# [ "students" ]
```

---

### `db.{collection-name}.drop()`

Remove a coleção da base de dados (em contexto), que fora especificada o comando `use`<sup>[2]</sup> (acima).

Exemplo de usagem:
```shell
# Usaremos como contexto a base de dados `school`:
use school

# Criaremos uma coleção `students`:
db.createCollection("students")

# Iremos remover a coleção `students`:
db.students.drop()
```
