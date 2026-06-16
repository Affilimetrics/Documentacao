## AFILLIMETRICS

### REQUISITOS FUNCIONAIS E NÃO FUNCIONAIS

## O que é a Análise de Requisitos?

É um estudo onde os requisitos funcionais descrevem **o que** o sistema deve fazer (como cadastrar usuários, exibir vendas e gerar relatórios), enquanto os requisitos não funcionais definem **como** o sistema deve se comportar em termos de desempenho, segurança, usabilidade e disponibilidade (como carregar o dashboard em até 3 segundos ou criptografar senhas), sendo ambos essenciais para garantir que o software atenda às necessidades dos usuários e aos padrões de qualidade exigidos pelo mercado.

---

## 1. Visão Geral

O sistema proposto consiste em uma plataforma web que permite aos
**afiliadores** gerenciar e acompanhar seu desempenho financeiro,
incluindo vendas, comissões, links ativos e métricas de conversão.

O objetivo principal é fornecer uma visualização clara e estratégica dos
resultados, auxiliando na tomada de decisões.

## 2. Stakeholders

- Afiliadores (usuários principais)
- Administrador do sistema
- Plataformas de afiliados (integração futura)

---

## REQUISITOS FUNCIONAIS

| ID | REQUISITO | CLASSIFICAÇÃO | DEPENDÊNCIAS |
|---|---|---|---|
| **RF01** | O sistema deve permitir **cadastro de usuários**, de forma que o usuário consiga criar uma conta com segurança. O formulário exigirá nome, e-mail, senha, CPF e número, com proteção contra múltiplas tentativas inválidas e 2FA via authenticator, incluindo bloqueio de acessos com credenciais inválidas depois de 5 tentativas e recuperação de senha, tendo como idade mínima 18 anos. O sistema deve conferir validação de CPF real conforme a base da Receita Federal, confirmação de número por SMS, e confirmação de e-mail por código. | Importante | -- |
| **RF02** | O sistema deve permitir que o usuário se **autentique** para acessar o módulo principal, exigindo que o usuário informe seu e-mail, senha e código authenticator, tendo a possibilidade de lembrar as credenciais. | Importante | RF01 |
| **RF03** | O sistema deve exibir o total de **vendas no dashboard**, importando as informações em tempo real baseado nas compras dos produtos cadastrados utilizando WebSocket para as atualizações, tendo a possibilidade de filtrar por dia, mês e ano. | Importante | -- |
| **RF04** | O sistema deve exibir o total de **comissões** baseado no cálculo do valor líquido das vendas de produtos cadastrados. | Importante | RF03 |
| **RF05** | O sistema deve exibir a **quantidade de links ativos** baseado na quantidade de produtos cadastrados. | Moderado | RF07 |
| **RF06** | O sistema deve exibir a **taxa de conversão**, utilizando a fórmula de número de conversões dividido por número de visitantes vezes 100. | Moderado | RF03, RF08 |
| **RF07** | O sistema deve permitir o **cadastro de links de afiliados**, de forma que o sistema consiga validar o link inserido e com a possibilidade de alterações por meio de edição e também deve conter a opção de pausar sem deletar o link. | Importante | RF01 |
| **RF08** | O sistema deve exibir **cliques por link**, utilizando rastreamento via server-side-tracking para identificar os cliques e exibindo ao lado de cada produto cadastrado. | Moderado | RF07 |
| **RF09** | O sistema deve apresentar **gráfico de vendas por período**, utilizando opção de filtragem para selecionar o período desejado. | Moderado | RF03 |
| **RF10** | O sistema deve exibir **vendas por categoria** fazendo o cálculo em porcentagem de qual categoria cada produto mais teve rendimento. | Desejável | RF03 |
| **RF11** | O sistema deve permitir **definir metas financeiras**. | Moderado | -- |
| **RF12** | O sistema deve exibir o **semáforo financeiro** (verde, amarelo, vermelho): verde quando a margem for de lucro, amarelo para zona de investimento e vermelho para prejuízo. | Importante | RF11 |
| **RF13** | O sistema deve gerar **alertas de prejuízo**, enviados como uma notificação no e-mail individual de cada usuário. | Moderado | RF03, RF04 |
| **RF14** | O sistema deve permitir **editar configurações do usuário**, tendo a opção para alteração de senha e exclusão de conta. | Importante | RF01, RF02 |
| **RF15** | O sistema deve **exibir gráfico ROI** (retorno sobre investimento). | Importante | RF01, RF02, RF03, RF04 |
| **RF16** | O sistema deve permitir **gerar relatório em PDF** com os dados do dashboard, incluindo vendas, comissões, taxa de conversão, cliques por link, gráficos e ROI, permitindo ao usuário selecionar o período desejado antes da geração. | Importante | RF03, RF04, RF06, RF08, RF09, RF15 |

---

## REQUISITOS NÃO FUNCIONAIS

| ID | REQUISITO | RESTRIÇÕES | DEPENDÊNCIAS |
|---|---|---|---|
| **RNF01** | O sistema deve possuir interface intuitiva e de fácil uso, de forma que usuários com uma primeira interação com sistemas financeiros consigam utilizar da melhor maneira. | Usabilidade | --|
| **RNF02** | O sistema deve carregar o dashboard em até 3 segundos. | Desempenho | RF03, RF04, RF05, RF06, RF09, RF10, RF12, RF15 |
| **RNF03** | O sistema deve garantir criptografia de senhas utilizando hash de senhas (bcrypt ou superior). O usuário deve utilizar no mínimo 8 caracteres, tendo que conter pelo menos 1 número e 1 caractere especial. | Segurança | RF01, RF02, RF14 |
| **RNF04** | O sistema deve utilizar protocolo HTTPS para todas as comunicações entre cliente e servidor. | Segurança | RF01, RF02, RF07, RF08, RF14 |
| **RNF05** | O sistema deve estar disponível 24 horas por dia, 7 dias por semana. | Disponibilidade | -- |
| **RNF06** | O sistema deve suportar múltiplos usuários simultâneos (mínimo de 1.000 usuários concorrentes). | Escalabilidade | -- |
| **RNF07** | O sistema deve ser compatível com navegadores modernos, tais como Google Chrome, Mozilla Firefox, Microsoft Edge, Opera e Safari (últimas 2 versões de cada). | Compatibilidade | -- |
| **RNF08** | O sistema deve funcionar em dispositivos móveis a partir de 280px de largura (abordagem responsiva). | Mobilidade | -- |
| **RNF09** | O sistema deve possuir código organizado e documentado (código comentado, README atualizado). | Manutenibilidade | -- |
| **RNF10** | O sistema deve possuir rastreamento via Server-Side-Tracking (SST) para cliques e conversões. | Rastreabilidade | RF06, RF08 |
