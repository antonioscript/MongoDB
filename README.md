# MongoDB
**Guia dos Principais Comandos do Banco de Dados Não Relacional MongoDB**

> To know how the integration with an api in. net click on this link below
> https://github.com/antonioscript/MongoDB.NET/edit/master/README.md


## Índice

- [Mostrar todos os bancos de dados](#mostrar-todos-os-bancos-de-dados)
- [Selecionar banco de dados](#selecionar-banco-de-dados)
- [Mostrar collections (tabelas)](#mostrar-collections-tabelas)
- [Criar uma collection](#criar-uma-collection)
- [Inserir um documento](#inserir-um-documento)
- [Inserir múltiplos documentos](#inserir-múltiplos-documentos)
- [Visualizar todos os documentos de uma collection](#visualizar-todos-os-documentos-de-uma-collection)
- [Limitar visualização de documentos](#limitar-visualização-de-documentos)
- [Buscar documento específico](#buscar-documento-específico)
- [Contar quantidade de registros](#contar-quantidade-de-registros)
- [Remover documento](#remover-documento)
- [Atualizar documento](#atualizar-documento)
- [References](#references)

---

## Mostrar todos os bancos de dados

```javascript
show dbs
```

## Selecionar banco de dados

```javascript
use banco_exemplo
```

## Mostrar collections (tabelas)

```javascript
show collections
```

## Criar uma collection

```javascript
db.createCollection("nome_da_collection")
```

## Inserir um documento

```javascript
db.nome_collection.insertOne({
  "nome": "Fulano",
  "Senha": 123
})
```

## Inserir múltiplos documentos

```javascript
db.itens.insertMany([
  {
    "name": "João",
    "price": 32
  },
  {
    "name": "Mateus",
    "price": 14
  },
  {
    "name": "Tiago",
    "price": 90
  }
])
```

## Visualizar todos os documentos de uma collection

```javascript
db.nome_collection.find()
```

## Limitar visualização de documentos

```javascript
db.nome_collection.find().limit(1)
```

## Buscar documento específico

```javascript
db.nome_collection.find({ "name": "João" })
```

## Contar quantidade de registros

```javascript
db.nome_collection.countDocuments()
```

## Remover documento

```javascript
db.nome_collection.deleteOne({ "name": "Tiago" })
```

## Atualizar documento

```javascript
db.nome_collection.updateOne(
  { "name": "João" },
  { $set: { "price": 99 } }
)
```

# References
https://www.mongodb.com/pt-br/docs/manual/crud/
