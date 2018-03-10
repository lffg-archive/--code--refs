# Testes

Abaixo listam-se os pacotes de testes disponíveis para JavaScript.  

Atualmente, estão listados:

- [Mocha](#mocha).

## Mocha

Mocha é um pacote NPM responsável por criar testes.  
Ele roda no terminal os testes.

Arquivo `package.json`:
```json
{
  "scripts": {
    "test": "./node_modules/.bin/mocha tests/**/*.spec.js"
  }
}
```
_**Nota:** Caminhos podem ser alterados._

Para rodar no terminal, basta executar o comando:
```shell
npm test
```

Alguns parâmetros podem ser passados:

- `--reporters`: Irá listar todos os tipos de _reporters_ que podem ser usados.

- `--reporter={}`: Irá definir um _reporter_ para os testes. As opções podem ser verificadas com o parâmetro acima.
   - _Para utilizar, basta trocar as chaves (`{}`) pelo nome do _reporter_ desejado.

- `--bail`: Irá parar a execução dos testes caso um deles falhe.
   - Isso é útil quando temos diversos testes, e não queremos rodar todos caso um deles dê erro.
   - Ajuda a encontrar uma falha mais facilmente.
