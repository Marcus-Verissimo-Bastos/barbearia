# Barbearia - Agendamento

Sistema bem básico de agendamento para barbearia, feito com Node.js, Express e JavaScript puro.
Os agendamentos ficam salvos no arquivo `agendamentos.json` (não precisa de banco de dados).

## O que faz

- Escolher serviço, barbeiro, data e horário
- Mostra só os horários livres do barbeiro naquele dia
- Não deixa marcar dois clientes no mesmo horário com o mesmo barbeiro
- Lista os agendamentos e permite cancelar

## Como rodar

```bash
npm install
npm run dev
```

Abra http://localhost:3000

(`npm start` roda sem reinício automático.)

## Mudar serviços, preços e barbeiros

Edite as listas `SERVICOS` e `BARBEIROS` no começo do `server.js`.
Os horários (09:00 às 17:00) ficam em `HORARIOS`, no mesmo arquivo.

## Rotas da API

| Método | Rota                      | O que faz                                  |
| ------ | ------------------------- | ------------------------------------------ |
| GET    | `/api/servicos`           | Lista os serviços                          |
| GET    | `/api/barbeiros`          | Lista os barbeiros                         |
| GET    | `/api/horarios`           | Horários livres (`data` e `barbeiro_id`)   |
| GET    | `/api/agendamentos`       | Lista os agendamentos                      |
| POST   | `/api/agendamentos`       | Cria um agendamento                        |
| DELETE | `/api/agendamentos/:id`   | Cancela um agendamento                     |

## Estrutura

```
barbearia/
├── front/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── server.js
├── nodemon.json
├── package.json
└── README.md
```
