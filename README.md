# 🎬 Modelagem de Dados em Grafos para um Serviço de Streaming

Projeto desenvolvido para o desafio **“Modelagem de Dados em Grafos de um Serviço de Streaming”**, com foco na criação de um modelo de dados em Neo4j para representar usuários, títulos (filmes e séries), gêneros, atores, diretores e interações de consumo.

---

## 📌 Objetivo

Modelar e implementar um pequeno grafo de conhecimento para um serviço de streaming, incluindo:

- Entidades (nós): `User`, `Movie`, `Series`, `Genre`, `Actor`, `Director`
- Relacionamentos:  
  - `WATCHED` (com propriedade `rating`)
  - `ACTED_IN`
  - `DIRECTED`
  - `IN_GENRE`
- Criação de constraints de unicidade
- Carga mínima com:
  - **10 usuários**
  - **10 títulos (filmes/séries)**
  - Relacionamentos entre entidades

---

## 🧠 Modelo Conceitual

### Nós
- **User**: usuário da plataforma
- **Movie**: filme
- **Series**: série
- **Genre**: gênero
- **Actor**: ator/atriz
- **Director**: diretor(a)

### Relacionamentos
- `(User)-[:WATCHED {rating}]->(Movie|Series)`
- `(Actor)-[:ACTED_IN]->(Movie|Series)`
- `(Director)-[:DIRECTED]->(Movie|Series)`
- `(Movie|Series)-[:IN_GENRE]->(Genre)`

---

