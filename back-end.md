# mLabs - Teste back-end

Este projeto tem como objetivo testar os conhecimentos, código e a organização do candidato.

# O projeto

Criar uma API de controle de estacionamento (conforme contratos abaixo):

  - Deve registrar entrada, saída e pagamento
  - Não deve liberar saída sem pagamento
  - Deve fornecer um histórico por placa

Essa API deve respeitar os status http corretamente, deve aceitar requisições e responder json.

## Ações que devem ser disponíveis

### Entrada

```
POST /parking

{ plate: 'FAA-1234' }
```

Deve retornar um número de "reserva" e validar a máscara AAA-9999

### Saída

```
PUT /parking/:id/out
```

### Pagamento

```
PUT /parking/:id/pay
```

### Histórico

```
GET /parking/:plate
[
  { id: 42, time: '25 minutes', paid: true, left: false }
]
```

## Sobre testes

Quanto mais melhor! :)

## Tecnologias e instruções

-  O sistema deve ser escrito em ruby.
-  Usar git.
-  Caso necessário algum preparo antes de testar é necessário fornecer um INSTALL.md explicando o processo.

## Aquele plus (não obrigatório)
-  Usar algum gerenciador de docker (preferencialmente docker-compose).
-  Configurar os pipelines CI/CD para rodar os builds.
-  Criar um Dockerfile para ser usado no deploy de teste, porque iremos fazer deploy da aplicação no kubernetes para testar.

## Sobre a avaliação

Este projeto tem como objetivo testar como o dev realiza a divisão de classes, organiza o código e a qualidade de teste.

A descrição do projeto contem o mínimo exigido para considerar o sistema como funcional.

## Dúvidas

Quaisquer dúvidas que você venha a ter, consulte as issues para ver se alguém já não a fez e caso você não ache sua resposta, abra você mesmo uma nova issue!

Boa sorte e bora codar! \o/
