# mLabs - Teste front-end

O teste consiste em avaliar as habilidades com algumas tecnologias básicas no desenvolvimento front-end, tais como HTML, CSS e Javascript. Foque em propor uma solução com um design de código bem elaborado e preparado para o crescimento da aplicação.

Sinta-se livre para usar os frameworks, libs ou ferramentas que mais se sentir confortável, o que importa é a linha de raciocínio seguida ;)

# O projeto

Criar um dashboard de conexão de redes sociais.

  - Seguir o layout proposto [nesse link](/assets/fbc-001.png)
  - O projeto deve ser responsivo
  - Suporte para Chrome, Firefox e Safari
  - Deve ser possível fazer a conexão de redes sociais nos diferentes canais do dashboard
  - Ao clicar em "Adicionar" deve ser exibido um modal (layout disponível [nesse link](/assets/fbc-002.png))
  - O modal deve listar todas as páginas disponíveis para o usuário (API mockada disponível em https://demo2697181.mockable.io/pages)
  - Ao tentar conectar alguma rede social, a listagem de páginas na modal deve ser filtrada de acordo com a rede selecionada.
  - Ao selecionar uma página e clicar em "Próximo", a mesma deve ser exíbida no Dashboard (layout disponível [nesse link](/assets/fbc-003.png))

## Exemplo de retorno da API

```
GET https://demo2697181.mockable.io/pages
{
  "data": [
    {
      "id": 1,
      "name": "Page name",
      "url": "https://page-url.com",
      "picture": "https://image-url.com.br",
      "channel_key": "facebook"
    }
  ]
}
```

## Sobre testes

Quanto mais melhor! :)

## Tecnologias e instruções

-  Usar git.
-  Caso necessário algum preparo antes de testar é necessário fornecer um INSTALL.md explicando o processo.

## Aquele plus (não obrigatório)
- Ao dar reload na tela, salvar os canaís conectados anteriormente.
- Em um arquivo README.md explicar o que te levou a escolher tecnologia X ou Y

## Sobre a avaliação

Este projeto tem como objetivo testar como o dev realiza a divisão de componentes, organiza o código e a qualidade de teste.

A descrição do projeto contem o mínimo exigido para considerar o sistema como funcional.

## Dúvidas

Quaisquer dúvidas que você venha a ter, consulte as issues para ver se alguém já não a fez e caso você não ache sua resposta, abra você mesmo uma nova issue!

Boa sorte e bora codar! \o/
