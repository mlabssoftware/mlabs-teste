# mLabs - Teste front-end

O teste consiste em avaliar as habilidades com algumas tecnologias básicas no desenvolvimento front-end, tais como HTML, CSS e Javascript. Foque em propor uma solução com um design de código bem elaborado e preparado para o crescimento da aplicação. Queremos ver o básico bem feito.

O teste Front-End da mLabs é o mesmo para Júnior, Pleno e Sênior. Siga as instruções abaixo de acordo com o nível da vaga que se candidatou.

Caso queira implementar features de um nível acima ao qual está se candidatando, fique a vontade, porém o mais importante é que ao final do teste os requisitos obrigatórios do seu nível tenham sido feitos.

Para cada nível, espera-se que os requisitos do nível anterior sejam atendidos, sempre prevalecendo os itens de maior senioridade para sua vaga.

- Teste júnior: espera-se que os requisitos gerais e os requisitos de júnior sejam atendios
- Teste pleno: espera-se que os requisitos anteriores (gerais e júnior) e os de pleno sejam atendidos
- Teste sênior: espera-se que os requisitos anteriores (gerais, júnior e pleno) e os de sênior sejam atendidos

# O teste

O teste consiste em criar interfaces que possibilitem o usuário agendar uma publicação em algumas redes sociais, além de permitir que ele possa visualizar uma lista com os agendamentos por status de publicação.

Disponibilizamos o design da interface através do Figma [nesse link](https://www.figma.com/file/JYNYnwyXKa0N3m7myjF8Y4/v1?node-id=0%3A1). Através dele você poderá encontrar as definições de estilo como formas, cores, tamanhos e fontes. Além de conseguir rodar o protótipo navegável e entender o fluxo esperado.

Todos os assets podem ser exportados através do próprio figma. Toda a iconografia utilizada pode ser usada através do Fontawesome Free. Caso queira usar imagens para testar, recomendamos usar o [Unsplash](https://unsplash.com/).

Para saber um pouco mais de como usar o Figma no nosso teste, veja nosso [guia básico de Figma](https://github.com/mlabssoftware/mlabs-teste/blob/master/front-end/figma.md).

## Requisitos gerais

### *Projeto*

- É permitido o uso de quaisquer framework JavaScript (como Angular, Ember, React, Svelte, Vue etc) ou também o não uso de nenhum framework JavaScript
- Não é permitido o uso de framework CSS (como Bootstrap, Material, Semantic UI e outros). Nós queremos saber como você estrutura, organiza e escreve seus estilos
- Atender requisitos de semântica
- A interface deverá ser responsiva e respeitar o design proposto
- Seu teste deverá estar documentado e sua versão final hospedada em algum lugar (recomendamos Netlify ou Heroku)

### *Tela inicial*

- Botão "agendar post" redireciona o usuário para a Tela de Agendamento

### *Tela de agendamento*

- Deverão ser exibidas 6 redes sociais como opção: Instagram, Linkedin, Youtube, Pinterest, Twitter e Facebook. Sendo Instagram e Linkedin as únicas habilitadas para o usuário selecionar
- O campo de data deverá respeitar o formato "DD/MM/AAAA"
- O campo de hora deverá respeitar o formato "HH:MM"
- Ao selecionar a rede social, deverá aparecer uma simulação de como ficará esse post na área "Visualização do post"
- Enquanto não houver uma rede social, data e hora selecionadas o botão "Agendar" deverá estar desabilitado
- Fazer upload de somente 1 imagem
- Ao clicar em agendar, deverá exibir uma caixa de alerta com a informação de sucesso para o usuário e redirecioná-lo para a tela de listagem de agendamento

### *Tela listagem de agendamento*

- Deverá conter uma tabela exibindo as informações de posts agendados

## Requisitos por nível

### **Júnior**

### *Tela de agendamento*

- Selecionar uma rede social por vez para realizar o agendamento
- O preview do post não deverá conter scroll horizontal

### *Tela listagem de agendamento*

- A tabela de agendametos deve exibir somente informações do post que acabou de agendar


### **Pleno**

### *Geral*

- Queremos saber como você lida com consumo de conteúdo via request. Para isso, use nossos exemplos de JSON na seção **API** logo mais abaixo para consumi-lá e exibir informações previamente na interface
- Não precisa ser uma API sendo consumida por uma URL externa, indicamos que faça isso consumindo diretamente do JSON no projeto, porém, esperamos que toda a implementação de consumo desses dados sejam feitos da mesma forma que faria se estivesse consumindo externamente
- Use AJAX, axios, fetch o que achar melhor
- Não esperamos persistência desses dados em um Banco de Dados, porém, esperamos alguma persistência a nível de usuário


### *Tela de agendamento*

- As redes sociais disponíveis e seu status deverão ser consumidos de um JSON (modelo logo abaixo na seção API)
- Selecionar mais de uma rede social para realizar um agendamento
- Se houver mais de uma rede social selecionada, o preview do post deverá permitir um scroll horizontal para visualizar as demais simulações de posts
- O campo de data deverá abrir um componente de calendário funcional (pode criar um do zero ou usar qualquer um disponível)
- No campo "texto do post" deverá ser possível adicionar emojis através de um widget na própria tela (pode criar do zero ou usar qualquer um disponnível)
- Na coluna "Ações", ao clicar em "Preview" deverá abrir uma simulação de como ficou aquele post pra cada rede social que ele foi marcado

### *Tela listagem de agendamento*

- A tabela de agendametos deve exibir informações de posts passados que deverão ser consumidas de um JSON (modelo logo abaixo na seção API)
- O post atual agendado deverá ser exibido na mesma tabela e espera-se que ele seja persistido de alguma forma para o usuário ver na tela
- Essa tabela deve ser responsiva
- Deverá ser possível ordenar a tabela por data e status
- A informação sobre o campo status deverá ser consumido de um JSON (modelo abaixo na seção API) para um cruzamento de informação do statu no post com sua respectiva descrição


### Sênior

### *Geral*

- (Diferencial) - Sua aplicação pode estar bem embasada em performance web seguindo as boas práticas de https://web.dev/vitals/ um bom ranking no teste pode ser algo a mais: https://web.dev/measure/
- (Diferencial) - Acessibilidade: seguir as boas práticas

### *Tela de agendamento*

- Quando o usuário clicar em "Cancelar", verificar se algum dado foi preenchido no form de agendamento e caso tenha sido, informar ao usuário que ele perderá essas informações se desejar prossseguir
- Ao clicar no botão "Salvar rascunho", sua aplicação deverá persistir os dados desse post de alguma forma em que seja possível fecharmos a aba, ir novamente a tela inicial da sua aplicação, clicar em "Agendar post" e as informações salvas em Rascunho daquele último post deverão aparecer ali

### *Tela listagem de agendamento*

- Implemente um componente que filtre a tabela por status, possibilitando o usuário exibir, por exemplo, somente os posts com status "Não aprovado". O design desse componente fica livre para sua escolha.


## API de exemplo sugerida

Na pasta [db](https://github.com/mlabssoftware/mlabs-teste/blob/master/front-end/db) você encontra os arquivos JSON a serem usados no projeto.

Lembrando que você pode mudar as informações do JSON e até renomear o que quiser, desde que o que precisamos que seja exibido e a interação que pedimos seja atendida.

Arquivo **social-networks.json**
```
GET /social-networks
```

Arquivo **schedules-status.json**
```
GET /schedules/status
```

Arquivo **schedules.json**
```
GET /schedules

```

## O que esperamos

- Os requisitos gerais sejam cumpridos;
- Os requisitos de cada nível sejam cumpridos;
- Responsividade
- Consistência de código
- Semântica
- Reuso de código
- Separação dos conceitos e responsabilidades
- Interface componentizável
- Atenção aos detalhes
- Testes unitários

## O que seria legal de ver mas não é obrigatório

- Teste de regressão visual
- Offline first
- Micro interações fluídas
- Escreva no projeto um arquivo MD nos contando sobre suas decisões técnicas, as dificuldades que teve, funcionalidades e melhorias que implementaria caso fosse um projeto longa vida.

## Instruções

- Use o Git e hospede seu repositório no Github
- Faça commits separados de acordo com a evolução do seu teste, não faça 1 commit gigante ao final. Haja como se fosse um projeto real onde está trabalhando com mais pessoas
- Bem documentado, queremos saber o que instalar e como rodar, sem isso não é possível avaliar.


## Dúvidas

Quaisquer dúvidas procure nosso time de Recrutamento para que possamos entrar em contato.

Boa sorte e bora codar! \o/
