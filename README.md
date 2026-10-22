# Front-End – Sistema de Gestão de Pessoas

**Atividade 08 – Consumindo o Back-End no Front-End – CRUD**

**Professor:** Vitor Lima Santana  
**Aluno(a):** Nicolas Gentile
**Disciplina:** Programação Back-End

## 1. Objetivo

Desenvolver uma aplicação Front-End utilizando HTML, CSS e JavaScript para consumir uma API REST desenvolvida em Node.js, Express e MySQL/MariaDB.

A atividade tem como foco implementar o cadastro de pessoas utilizando o método HTTP **POST**, a função `fetch()` e o tratamento de erros com `async/await` e `try/catch`.

## 2. Tecnologias utilizadas

- HTML5
- CSS3
- JavaScript
- Fetch API
- Async/Await
- Try/Catch
- Node.js e Express (Back-End)
- MySQL/MariaDB (Banco de dados)

## 3. Estrutura do projeto

```text
frontend-gestao-pessoas/
│
├── index.html
├── cadastro.html
├── editar.html
│
├── css/
│   └── style.css
│
├── js/
│   ├── listar.js
│   ├── cadastro.js
│   └── editar.js
│
└── README.md
```

## 4. Funcionalidades

O sistema possui as seguintes operações:

| Método | Rota | Funcionalidade |
|---|---|---|
| GET | /pessoas | Listar pessoas |
| GET | /pessoas/:id | Consultar pessoa |
| POST | /pessoas | Cadastrar pessoa |
| PUT | /pessoas/:id | Atualizar pessoa |
| DELETE | /pessoas/:id | Excluir pessoa |

## 5. Implementação do POST

O aluno deverá desenvolver o arquivo `js/cadastro.js`, responsável por capturar os dados do formulário HTML e enviá-los para a API.

A implementação deverá utilizar:

- `addEventListener("submit", ...)`
- `preventDefault()`
- `async/await`
- `try/catch`
- `fetch()`
- `method: "POST"`
- `JSON.stringify()`
- Verificação de `resposta.ok`

### Exemplo da estrutura de requisição

```javascript
const resposta = await fetch(
  "http://localhost:3000/pessoas",
  {
    method: "POST",
    headers: {
      "Content-Type": "application/json"
    },
    body: JSON.stringify({
      nome,
      idade
    })
  }
);
```

O código deverá estar dentro de uma função assíncrona, com tratamento de erros utilizando `try/catch`.

O aluno também deverá validar os campos nome e idade antes de enviar os dados.

## 6. Como executar

### Back-End

1. Realizar o Fork do repositório original disponibilizado pelo professor.
2. Clonar o repositório.
3. Instalar as dependências:

```bash
npm install
```

4. Configurar a conexão com o banco de dados.
5. Iniciar a API:

```bash
npm start
```

A API estará disponível em:

`http://localhost:3000`

### Front-End

1. Abrir o projeto no Visual Studio Code.
2. Verificar se o Back-End está funcionando.
3. Executar `index.html` com o Live Server.
4. Acessar a página de cadastro.
5. Cadastrar uma pessoa.
6. Verificar se os dados foram armazenados no banco de dados.

## 7. Evidências

Adicione capturas de tela demonstrando:

**Imagem 1 – Tela de listagem**

![Listagem](./fotos/{8DB75EEE-87F1-4886-AA53-F4D27AEE5212}.png)

**Imagem 2 – Formulário de cadastro**

![Formulario de Cadastro](./fotos/{14769E59-D8AC-4CFA-9AA7-859059DA6623}.png)

**Imagem 3 – Cadastro funcionando**

![Foto cadastro](./fotos/{40EC9369-CC2B-4415-869D-5D33A08BA679}.png)

**Imagem 4 – Registro inserido no banco de dados**

![Banco de dados](./fotos/{56D30375-BD16-4554-9798-9FE11DF17D17}.png)

## 8. Repositórios

**Back-End (Fork):** [Inserir link]

**Front-End:** [Inserir link]

## 9. Conclusão do aluno

Explique com suas palavras:

- Como funciona a comunicação entre o Front-End e o Back-End?

- R: O Front-End envia uma requisição (request) pedindo dados ao Back-End, que processa a informação e devolve uma resposta (response) em formato JSON para a tela ser atualizada.

- Qual é a finalidade do método POST?
- R: A finalidade principal do método POST é enviar dados do Front-End para o Back-End para criar um novo recurso no servidor (como cadastrar um usuário, enviar uma mensagem ou fazer um pedido).

- Por que utilizamos `async/await` e `try/catch`?
- R: O async/await faz o código esperar a resposta da API antes de continuar, tornando a leitura sequencial e simples, enquanto o try/catch captura eventuais erros de conexão ou do servidor para evitar que a aplicação quebre.

- Quais dificuldades você encontrou durante a atividade?
- R: Fazer a ligação do banco de dados com o back-end

[Escreva sua conclusão aqui.]

---

## Créditos

**Professor responsável:** Vitor Lima Santana

**Desenvolvido por:** Nicolas 

**Atividade 08 – Desenvolvimento Web e Consumo de APIs REST**