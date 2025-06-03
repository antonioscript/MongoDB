# MongoDB
 Guia dos Princiapais Comandos do Banco de dados não Relacional MongoDB

# Comandos MongoDB

# Mostrar todos os bancos de dados
show dbs

# Seleciona aquele banco de dados
use banco_exemplo

# Mostra as collections (tabelas)
show collections

# Cria uma collection
db.createCollection("nome_da_collection")

# Para Inserir um documento
db.nome_collection.insert ({
    "nome": "Fulano",
    "Senha": 123
})

# Para Inserir vários itens
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

# Para Visualizar uma collection
db.nome_collection.find()

# Para visualizar apenas alguns itens
db.nome_collection.find().limit(1)

# Localizando um item específico
db.nome_collection.find({ "name": "João" })

# Retornar a quantidade de registros
db.nome_collection.find().count()

# Remover um registro
db.nome_collection.remove({ "name": "Tiago" })

# Atualizar um registro
db.nome_collection.update(
    { "name": "João" },
    { "$set": { "price": 99 } }
)
