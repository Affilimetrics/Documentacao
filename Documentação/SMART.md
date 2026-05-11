# Análise SMART - Affilimetrics

**Data:** 02/05/2026

## O que é o método SMART?

| Critério | Significado | Pergunta |
|----------|-------------|----------|
| **S** | Específico | O que de fato será feito? |
| **M** | Mensurável | Como o progresso é medido? |
| **A** | Atingível | O que fazer para alcançar a meta? |
| **R** | Relevante | De que maneira contribui para o projeto? |
| **T** | Temporal | Quando será realizado? Qual o prazo? |

---

## VIABILIDADE OPERACIONAL

### Objetivo 1 – Dashboard de Controle Financeiro

| Critério | Descrição |
|----------|-----------|
| **S** | Implementar dashboard principal com exibição de vendas (diárias, mensais e anuais), comissões, links ativos, taxa de conversão, metas financeiras e semáforo financeiro com cores padrão (verde, amarelo e vermelho). O sistema deve exibir os gráficos de Vendas por Categoria, Performance por Marketplace e Gráfico de ROI e sistema automatizado de Remarketing. |
| **M** | Gráficos devem ser interativos. Semáforo deve mudar de cor com base na meta. |
| **A** | O sistema deve utilizar gráficos interativos na análise de performance. |
| **R** | Permitir que o afiliado visualize seu desempenho em tempo real, identifique produtos mais lucrativos e tome decisões estratégicas, enviando notificações e auxiliando o afiliador para a melhor tomada de decisão. |
| **T** | Dashboard finalizado e testado, iniciando em 20 de junho e finalizado até 15 de outubro. |

**Descrição:**  
Será implementada uma tela principal que reunirá todas as métricas importantes para o afiliado em um só lugar. O dashboard exibirá o total de vendas, o valor de comissões recebidas, a quantidade de links ativos, Grafico de ROI, a taxa de conversão e um semáforo financeiro (verde, amarelo, vermelho) que indica se o afiliado está atingindo suas metas, notificações para auxiliar na tomada de decições e sistema automatizado de Remarketing.

---

### Objetivo 2 – Segurança e Conformidade

| Critério | Descrição |
|----------|-----------|
| **S** | O sistema deve implementar medidas de segurança para proteger dados pessoais dos afiliados e seus clientes garantindo conformidade com a LGPD, tais como, proteção utilizando Hash de Senhas, comunicações em HTTPS e 2FA via Authenticator. |
| **M** | 100% das senhas devem ser armazenadas com segurança. 100% das comunicações devem usar HTTPS. O sistema deve permitir exportar e excluir dados do usuário. |
| **A** | Utilizar ferramentas para proteção de senhas e HTTPS com certificado SSL/TLS. |
| **R** | Evitar multas, proteger a imagem do sistema e garantir a confiança dos afiliados. |
| **T** | Medidas implementadas até a data de lançamento do sistema. |

**Descrição:**  
Serão implementadas medidas técnicas para proteger os dados pessoais dos afiliadores e dos clientes que acessarem os links. Todas as senhas serão criptografadas antes de serem armazenadas no banco de dados. Todas as comunicações serão feitas exclusivamente via HTTPS com certificado SSL/TLS, garantindo conformidade com a LGPD.

---

## VIABILIDADE TÉCNICA

### Objetivo 1 – Cadastro e Autenticação de Usuários

| Critério | Descrição |
|----------|-----------|
| **S** |    |
| **M** | 100% dos usuários devem conseguir se cadastrar e acessar o sistema. O sistema deve bloquear acessos com credenciais inválidas. |
| **A** | O sistema deve conter front-end estruturado, Django no back-end, PostgreSQL no banco de dados, Django para hash de senhas e Rastreamento via Sever-Side-Tracking para gerenciamento de sessão. |
| **R** | Garantir que apenas usuários autorizados acessem dados pessoais e financeiros, conforme exigido pela LGPD. |
| **T** | Módulo finalizado e testado iniciando em 5 de junho, até 1 de outubro |

**Descrição:**  


