# 🧪 Postman API Test Collections - QA Manual Testing

Este repositório contém coleções de testes para APIs RESTful desenvolvidas no Postman com foco em teste manual e testes exploratórios de QA. 
As coleções foram organizadas por domínio funcional, com ambiente configurável e scripts de teste em cada requisição.

---

## 📁 Estrutura do Projeto

```shell
Api-Post/
├── collection/             
│   └── Api - Posts.postman_collection.json   
├── environment/            
│   └── Api-post-environment.postman_environment.json
└── README.md         
```

      
## 🧰 Pré-requisitos

- [Postman Desktop App](https://www.postman.com/downloads/) ou [Postman Web](https://web.postman.com/)
- Permissão de acesso às APIs que serão testadas
- Variáveis do ambiente corretamente preenchidas


## 📂 Coleções Disponíveis

As coleções estão localizadas na pasta `collection/` e organizadas por escopo funcional da API.

| Coleção | Descrição |
|--------|-----------|
| `Api - Posts.postman_collection.json` | Testes: Create, Update, Delete e Read Posts|

## 🌍 Ambientes

A pasta `environment/` contém os arquivos de ambiente utilizados pelas coleções. 

### Exemplo de variáveis no ambiente `dev`:

| Nome        | Valor exemplo                      | Descrição                       |
| ----------- | ---------------------------------- | ------------------------------- |
| `BASE_URL`   | `https://jsonplaceholder.typicode.com`   | URL base da API em ambiente dev |


Para carregar o ambiente no Postman:

1. Vá até **Environments > Import**
2. Selecione o arquivo `Api-post-environment.postman_environment.json`
3. Ative o ambiente desejado no canto superior direito da interface
# 🧪 Suite de Testes: Posts API

## 📌 Casos de Teste

| ID      | Título                     | Descrição                                         | Resultado Esperado |
|---------|----------------------------|---------------------------------------------------|--------------------|
| CT-001  | Listar todos os posts      | Validar que a API retorna a lista de posts        | Retorna **100 posts em JSON** com **status 200** |
| CT-002  | Obter post por ID válido   | Validar que a API retorna um post existente       | Retorna o **post correspondente** com **status 200** |
| CT-003  | Obter post inexistente     | Validar que a API não retorna post inválido       | Retorna **Not Found** com **status 404** |
| CT-004  | Criar um post válido       | Validar que a API cria um novo post               | Retorna **post criado com ID** com **status 201** |
| CT-005  | Alterar post por ID        | Validar que a API atualiza corretamente um post   | Retorna **dados alterados** com **status 200** |
| CT-006  | Deletar post por ID        | Validar que a API deleta corretamente um post     | Retorna **sem conteúdo** com **status 204** |

## 🧪 Executando os Testes Manualmente

1. **Importe as coleções**:
   - Acesse o Postman > `Collections > Import`
   - Selecione o arquivo `Api - Posts.postman_collection.json ` desejado

2. **Importe o ambiente**:
   - Vá em `Environments > Import`
   - Selecione o arquivo `.Api-post-environment.postman_environment.json`

3. **Execute os testes**:
   - Vá até a coleção desejada
   - Clique com o botão direito e selecione  run
   - Escolha o ambiente e execute
