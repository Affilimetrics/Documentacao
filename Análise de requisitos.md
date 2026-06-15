## AFILLIMETRICS

### REQUISITOS FUNCIONAIS E NÃO FUNCIONAIS

## Oque é a Análise de Requisitos?

É um estudo, onde os requisitos funcionais descrevem **o que** o sistema deve fazer (como cadastrar usuários, exibir vendas e gerar relatórios), enquanto os requisitos não funcionais definem **como** o sistema deve se comportar em termos de desempenho, segurança, usabilidade e disponibilidade (como carregar o dashboard em até 3 segundos ou criptografar senhas), sendo ambos essenciais para garantir que o software atenda às necessidades dos usuários e aos padrões de qualidade exigidos pelo mercado.

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

| ID     | REQUISITO                                      | CLASSIFICAÇÃO | DEPENDÊNCIAS          |
|--------|------------------------------------------------|---------------|-----------------------|
| **RF01**   | O sistema deve permitir **cadastro de usuários**, de forma que, o usuario consiga criar uma conta com segurança, o formulario exigirá nome, e-mail, senha, CPF e número, com proteção contra múltiplas tentativas inválidas e 2FA via authenticator incluindo bloqueio de acessos com credenciais inválidas depois de 5 tentativas e recuperação de senha, tendo como sua idade minima 18, o sistema deve conferir validação de cpf real conforme a base da receita federal, confirmação de numero por SMS, e confirmação de email por codigo.       | Importante    | **--**                |
| **RF02**   | O sistema deve permitir que o usuario se **autentique** para acessar o modulo principal exigindo que o usuario informe seu email senha e codigo autehnticator e tendo a possibilidade de lembrar as credenciais.        | Importante    | **RF01**              |
| **RF03**   | O sistema deve exibir o total de **vendas no dashboard**, importando as informaçoes em tempo real baseado nas compras dos produtos cadastrados utilizando WebSocket para as atualizaçoes, tendo a possibilidade de filtrar por dia mes e ano.    | Importante    | **--**                |
| **RF04**   | O sistema deve exibir o total de **comissões** baseado no calculo do valor liquido das vendas de produtos cadastrados.              | Importante    | **RF03**              |
| **RF05**   | O sistema deve exibir a quantidade de links ativos baseado na quantidade de produtos cadastrados.      | Moderado      | **RF07**              |
| **RF06**   | O sistema deve exibir a taxa de conversão.               | Moderado      | **RF03, RF08**        |
| **RF07**   | O sistema deve permitir o cadastro de links de afiliados.| Importante    | **RF01**              |
| **RF08**   | O sistema deve exibir cliques por link.                  | Moderado      | **RF07**              |
| **RF09**   | O sistema deve apresentar gráfico de vendas por período. | Moderado      | **RF03**              |
| **RF10**   | O sistema deve apresentar gráfico de cliques.            | Moderado      | **RF08**              |
| **RF11**   | O sistema deve exibir vendas por categoria.              | Desejável     | **RF03**              |
| **RF12**   | O sistema deve permitir definir metas financeiras.       | Moderado      | **--**                |
| **RF13**   | O sistema deve exibir o semáforo financeiro (verde, amarelo, vermelho). | Importante | **RF12** |
| **RF14**   | O sistema deve gerar alertas de prejuízo.                | Moderado      | **RF03, RF04**        |
| **RF15**   | O sistema deve permitir editar configurações do usuário. | Importante    | **RF01, RF02**        |
| **RF16**   | O sistema deve exibir grafico ROI(retorno sobre investimento). | Importante    | **RF01, RF02**        |

---

## REQUISITOS NÃO FUNCIONAIS

| ID      | REQUISITO                                                   | CLASSIFICAÇÃO | DEPENDÊNCIAS                         |
|---------|-------------------------------------------------------------|---------------|--------------------------------------|
| **RNF01**  | O sistema deve possuir interface intuitiva e de fácil uso.            | Importante    | **** |
| **RNF02**  | O sistema deve carregar o dashboard em até 3 segundos.                | Importante    | ****                     |
| **RNF03**  | O sistema deve garantir criptografia de senhas.                       | Importante    | ****                            |
| **RNF04**  | O sistema deve utilizar protocolo HTTPS.                              | Importante    | ****                            |
| **RNF05**  | O sistema deve estar disponível 24 horas por dia.                     | Importante    | ****                               |
| **RNF06**  | O sistema deve suportar múltiplos usuários simultâneos.               | Moderado      | ****                            |
| **RNF07**  | O sistema deve ser compatível com navegadores modernos.               | Importante    | ****                               |
| **RNF08**  | O sistema deve funcionar em dispositivos móveis.                      | Importante    | ****                     |
| **RNF09**  | O sistema deve possuir código organizado e documentado.               | Moderado      | ****                               |
| **RNF10**  | O sistema deve possuir rastreamento via Server-Side-Tracking.         | Moderado      | ****                            |
