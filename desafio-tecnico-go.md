# Desafio Técnico - Go(lang)

**O desafio é criar uma API de transferencia entre contas Internas de um banco digital.**

=====================
#### API

#### Regras gerais

* Usar formato JSON para leitura e escrita. (ex: `GET /accounts/` retorna json, `POST /accounts/ {name: 'james bond'}`)

#### Rotas esperadas

##### `/accounts`

Espera-se as seguintes ações:

- obtém a lista de contas
- obtém o saldo da conta
- cria uma conta

*Regras para esta rota*

- `balance` pode iniciar com 0 ou algum valor para simplificar
- `secret` deve ser armazenado como hash

* * *
##### `/login`

Espera-se as seguintes ações:

- autentica a usuaria

*Regras para esta rota*

- Deve retornar token para ser usado nas rotas autenticadas
* * * 

##### `/transfers`

Espera-se as seguintes ações:

- obtém a lista de transferencias da usuaria autenticada.
- faz transferencia de uma conta para outra.

*Regras para esta rota*

- Quem fizer a transferência precisa estar autenticada.
- O conta de origem deve ser obtido no Token enviado.
- Caso a conta de origem não tenha saldo, retornar um código de erro apropriado
- Atualizar o balance das contas

=====================

### Requisitos Técnicos

- O código do desafio estar na linguagem [Go](https://golang.org/)
- Pode-se utilizar qualquer package ou framework, mas lembre-se: stdlib > packages > frameworks (usar standard library do Go é melhor que usar packages, que é melhor que usar frameworks...)
- Utilização de Docker é obrigatório
