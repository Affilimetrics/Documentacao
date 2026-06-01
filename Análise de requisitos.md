## AFILLIMETRICS

### REQUISITOS FUNCIONAIS E NÃO FUNCIONAIS

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
| **RF01**   | O sistema deve permitir cadastro de usuários.            | Importante    | **--**                |
| **RF02**   | O sistema deve permitir login com email e senha.         | Importante    | **RF01**              |
| **RF03**   | O sistema deve exibir o total de vendas no dashboard.    | Importante    | **--**                |
| **RF04**   | O sistema deve exibir o total de comissões.              | Importante    | **RF03**              |
| **RF05**   | O sistema deve exibir a quantidade de links ativos.      | Moderado      | **RF07**              |
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

---

## REQUISITOS NÃO FUNCIONAIS

| ID      | REQUISITO                                                   | CLASSIFICAÇÃO | DEPENDÊNCIAS                         |
|---------|-------------------------------------------------------------|---------------|--------------------------------------|
| **RNF01**  | O sistema deve possuir interface intuitiva e de fácil uso.            | Importante    | **RNF02, RNF05, RNF06, RNF07, RNF08** |
| **RNF02**  | O sistema deve carregar o dashboard em até 3 segundos.                | Importante    | **RNF05, RNF06**                     |
| **RNF03**  | O sistema deve garantir criptografia de senhas.                       | Importante    | **RNF04**                            |
| **RNF04**  | O sistema deve utilizar protocolo HTTPS.                              | Importante    | **RNF07**                            |
| **RNF05**  | O sistema deve estar disponível 24 horas por dia.                     | Importante    | **--**                               |
| **RNF06**  | O sistema deve suportar múltiplos usuários simultâneos.               | Moderado      | **RNF05**                            |
| **RNF07**  | O sistema deve ser compatível com navegadores modernos.               | Importante    | **--**                               |
| **RNF08**  | O sistema deve funcionar em dispositivos móveis.                      | Importante    | **RNF05, RNF01**                     |
| **RNF09**  | O sistema deve possuir código organizado e documentado.               | Moderado      | **--**                               |
| **RNF10**  | O sistema deve possuir rastreamento via Server-Side-Tracking.         | Moderado      | **RNF05**                            |
