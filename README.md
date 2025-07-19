# banco-api-tests

## Introdução

Este projeto reúne testes automatizados para a API REST do [banco-api](https://github.com/juliodelimas/banco-api), desenvolvidos durante as aulas práticas da mentoria do Júlio de Lima voltadas para testes de API. O foco está em validar os principais fluxos da aplicação com testes de integração, utilizando ferramentas amplamente adotadas no mercado.

## Tecnologias Utilizadas

- **Node.js** com **JavaScript**
- **Mocha** – framework de testes
- **Chai** – biblioteca de asserções
- **Supertest** – para requisições HTTP
- **Mochawesome** – geração de relatórios em HTML
- **dotenv** – gerenciamento de variáveis de ambiente via `.env`

## Estrutura do Repositório

```
banco-api-tests/
├── test/                    # Testes organizados por funcionalidades
│   ├── login.test.js
│   └── transferencias.test.js
├── mochawesome-report/     # Relatório HTML gerado automaticamente após a execução
├── .env                    # Variável BASE_URL da API testada
├── .gitignore
├── package.json
└── README.md
```

## Objetivo de Cada Grupo de Arquivos

- `test/`: contém os arquivos de teste separados por funcionalidade da API.
- `mochawesome-report/`: pasta gerada automaticamente com o relatório visual dos testes.
- `.env`: onde é definida a variável `BASE_URL`, apontando para a URL da API.
- `package.json`: lista dependências e scripts de execução dos testes.
- `README.md`: este guia de referência para uso do projeto.

## Instalação e Execução

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/banco-api-tests
   cd banco-api-tests
   ```

2. Crie um arquivo `.env` com a URL da API:
   ```env
   BASE_URL=http://localhost:3000
   ```

3. Instale as dependências:
   ```bash
   npm install
   ```

4. Execute os testes:
   ```bash
   npm test
   ```

5. O relatório em HTML será salvo em:
   ```
   mochawesome-report/mochawesome.html
   ```

### Dica: abrir o relatório automaticamente

Adicione este script no `package.json`:

```json
"scripts": {
  "test:report": "npm test && start mochawesome-report/mochawesome.html"
}
```

(Substitua `start` por `open` se estiver no macOS ou Linux.)
