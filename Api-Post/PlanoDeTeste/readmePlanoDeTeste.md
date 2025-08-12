Plano de Testes com Postman – API de Posts

### **Identificação do Projeto**

- **Projeto:** API - Lista de Posts

- **Responsável pelo Teste:** Rômulo Sérgio

- **Ferramenta de Teste:** Postman

---

### **Objetivo do Teste**

- Validar os principais endpoints da API
- Verificar os códigos  HTTP estão de acordo com a documentação 
-  Garantir que o sistema funcione como o esperado

---

### **Endpoints da API**

Base URL: https://jsonplaceholder.typicode.com/ 


| Metodo | Endpoint      | Funcionalidade            |
| ------ | ------------- | ------------------------- |
| GET    | /posts     | Listar todos posts existentes |
| GET    | /posts/:id | Obter o posts com o ID  |
| POST   | /posts     | Criar um post novo       |
| PUT    | /posts/:id | Alterar um posts pelo ID |
| DELETE | /posts/:id | Deletar um posts pelo ID      |
---

### Caso de Teste

| ID           | Endpoint   | Metodo | Descrição do teste                | Dados de Entrada                                           | Saída Esperada             | Status Code |
| ------------ | ---------- | ------ | --------------------------------- | ---------------------------------------------------------- | -------------------------- | ----------- |
| CT -001      | /posts     | GET    | Listar todos os posts             | -                                                          | lista de 100 posts em JSON | 200         |
| CT - 002     | /posts/:id | GET    | Obter um posts por ID             | - ID valido                                                | Post do ID                 | 200         |
| CT - 003     | /posts/:id | GET    | Obter post inexistente            | - ID invalido                                              | Not found                  | 404         |
| CT - 003     | /posts     | POST   | Criar um post                     | { "title": "testando API", "body": "body do teste de api"} | Post criado com ID         | 201         |
| CT - 004 | /posts     | POST   | Criar um post invalido sem o BODY | {"title": testes}                                          | Erro na criação            | 400         |
| CT - 005     | /posts/:id | PUT    | Alterar o post com ID             | { "title": testes2, "body": testes2}                       | Dados Alterados            | 200         |
| CT - 006     | /posts/:id | DELETE | Deletar um post                   | - ID valido                                                | Dado deletado              | 204         |

---

### **Ferramentas Utilizadas**

- **Postman** (coleções manuais)