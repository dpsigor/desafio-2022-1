# Desafio para o processo seletivo IR FLASH 2022/01

Repositório destinado aos interessados em participar do processo seletivo da IR FLASH 2022/01. As vagas são voltadas para desenvolvimento de aplicações Web.

## Sobre a IR FLASH

Investidores na [Bovespa e BM&F](https://www.b3.com.br/pt_br/) devem declarar seus lucros e prejuízos à Receita Federal, entre outras informações, e recolher impostos devidos.

Os cálculos impõem sobre as pessoas físicas um trabalho moroso, complexo e suscetível a erros, de forma que milhões de brasileiros correm o risco de sofrer multas e ter seu CPF negativado todos os meses.

O [aplicativo IR Flash](https://www.irflash.com.br) fornece o cálculo sobre as operações na bolsa para investidores, gestores e contadores. Acreditamos que a gestão de operações na Bolsa deve ser maximamente automatizado e simplificado, permitindo ao investidor focar a atenção em seus investimentos. Nosso aplicativo já beneficiou centenas de usuários.

## Sobre a vaga

Temos duas vagas para prestadores de serviço de desenvolvimento web.

Os desenvolvedores que atuam com a IR Flash são responsáveis por criar e manter aplicações para clientes internos e externos, prover soluções escaláveis, resilientes e altamente disponíveis que sustentem picos de acesso além de atuar como referência técnica e tutores de outros desenvolvedores.

Procuramos por pessoas dinâmicas, motivadas e que queiram estar aprendendo sempre. Se você tem esse perfil, é autoconfiante, autodidata e tem facilidade para lidar com desafios diários, essa vaga é para você!

# O Desafio

Construir aplicação web de cadastro de operações de compra e venda.

## Aplicação

- A tela inicial consiste em uma tela de login ou cadastro.
- Ao autenticar-se, o usuário é navegado para uma tela que apresente as operações já cadastradas.
- Uma operação consiste nos seguintes dados: data (ano, mês e dia), nome da corretora, CV (compra ou venda), ticker (identificador do ativo negociado), quantidade (número inteiro) e preço unitário. Exemplo:

```json
{
  "data": "2022-05-09",
  "corretora": "XP",
  "CV": "C",
  "ticker": "PETR4",
  "qtd": 100,
  "prc": 32.49"
}
```

- O usuário pode cadastrar novas operações com um formulário.
- O usuário pode editar operações.
- O usuário pode remover operações.
- Em outro componente, o usuário pode consultar sua custódia, que consiste na consolidação de todas suas operações. Exemplo:
    1. Em 02/05/2022, comprou na corretora XP a quantidade de 100 PETR4 a R\$30,00 cada. Custódia: XP - posição comprada - PETR4 - qtd 100 - valor R\$3000,00
    1. Em 03/05/2022, comprou na corretora XP a quantidade de 200 PETR4 a R\$32,00 cada. Custódia: XP - posição comprada - PETR4 - qtd 300 - valor R\$9400,00
    1. Em 04/05/2022, vendeu na corretora XP a quantidade de 50 PETR4 a R\$31,00 cada. Custódia: XP - posição comprada - PETR4 - qtd 250 - valor R\$7833,33
    - Portanto, o componente de custódia deve exibir essa última informação.
    - As custódias em corretoras diferentes não se afetam.
    - Note que o preço de venda não afeta o valor da custódia no exemplo, pois o valor é o valor despendido com as compras.
    - É possível haver custódia em posição vendida.

### Requisitos de código

- Utilizar no frontend o framework Angular.
- O backend e o banco de dados ficam a critério do candidato.
- Utilizar uma ferramenta de lint como [eslint](https://github.com/eslint/eslint).

### Aprimoramentos adicionais da aplicação (opcional)

A aplicação criada para o desafio pode ser aprimorada com recursos pensados por você. A seguir, foram listadas algumas sugestões do que poderia ser feito:

- Testes
- Documentação

## O que devo entregar?

- Esperamos de você duas entregas: apenas o código no GitHub e um vídeo explicativo no YouTube.

### Mas, afinal, quais ferramentas a IR Flash utiliza?

* Front-end: [Angular](https://angular.io/)
* Back-end: [Node.js](https://nodejs.org/en/) e [Go](https://golang.org/)
* Banco de dados: [MongoDB](https://www.mongodb.com/)
* Containers: [Docker](https://www.docker.com/)
* CI/CD: [GitHub Actions](https://github.com/features/actions)

### Instruções

- Faça um fork desse repositório.
- Em seguida, crie uma branch, cujo nome é o seu nome completo, no seguinte formato: meu-nome-completo.
- Resolva o desafio realizando versionamento local e remoto. Fique à vontade em criar outras branches durante o desenvolvimento do código.
- Inclua no README.md uma breve instrução de instalação e de execução da aplicação criada.
- Faça um vídeo que explique o que você fez no desafio, com duração aproximada de 5 minutos. A facecam é opcional, mas bem-vinda. O vídeo deve ser postado no YouTube (pode deixar como não listado) e seu link deve ser colocado no README.md.
- Ao finalizar o desafio, faça um pull request de sua branch para esse repositório.

### Prazo limite de entrega

O pull request com sua solução do desafio deve ser feito até a data especificada no corpo do email que você recebeu com a descrição do desafio.
