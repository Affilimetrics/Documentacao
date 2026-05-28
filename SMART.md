# Análise SMART - Affilimetrics

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
| **M** | Gráficos devem ser interativos e devem ser exibidos com informações condizentes. O semáforo deve mudar de cor com base na meta, e deve haver envio de notificações para remarketing. |
| **A** | Utilizar Django para criação de gráficos interativos, implementar a lógica de um semáforo financeiro comparando, no back-end, vendas reais com a meta cadastrada, e configurar sistema de notificação por remarketing. |
| **R** | Permitir que o afiliado visualize seu desempenho em tempo real, identifique produtos mais lucrativos e tome decisões estratégicas, enviando notificações e auxiliando o afiliado para a melhor tomada de decisão. |
| **T** | Dashboard finalizado e testado, iniciando em 20 de junho e finalizado até 15 de outubro. |

**Descrição:**  
Será implementada uma tela principal que reunirá todas as métricas importantes para o afiliado em um só lugar. O dashboard exibirá o total de vendas, o valor de comissões recebidas, a quantidade de links ativos, gráfico de ROI, a taxa de conversão e um semáforo financeiro (verde, amarelo, vermelho) que indica se o afiliado está atingindo suas metas, com notificações para auxiliar na tomada de decisões e sistema automatizado de remarketing.

---

### Objetivo 2 – Segurança e Conformidade

| Critério | Descrição |
|----------|-----------|
| **S** | O sistema deve implementar medidas de segurança para proteger dados pessoais dos afiliados e seus clientes, garantindo conformidade com a LGPD, tais como proteção utilizando hash de senhas, comunicações em HTTPS e 2FA via authenticator. |
| **M** | 100% das senhas devem ser armazenadas com segurança. 100% das comunicações devem usar HTTPS. O sistema deve permitir exportar e excluir dados do usuário. |
| **A** | Utilizar ferramentas para proteção de senhas e HTTPS com certificado SSL/TLS, e implementar hash de senhas utilizando Django e 2FA via authenticator. |
| **R** | Evitar multas, proteger a imagem do sistema e garantir a confiança dos afiliados. |
| **T** | Medidas implementadas até a data de lançamento do sistema. |

**Descrição:**  
Serão implementadas medidas técnicas para proteger os dados pessoais dos afiliados e dos clientes que acessarem os links. Todas as senhas serão criptografadas antes de serem armazenadas no banco de dados. Todas as comunicações serão feitas exclusivamente via HTTPS com certificado SSL/TLS, garantindo conformidade com a LGPD.

---

## VIABILIDADE TÉCNICA

### Objetivo 1 – Cadastro e Autenticação de Usuários

| Critério | Descrição |
|----------|-----------|
| **S** | Desenvolver módulo completo de cadastro de novos usuários com nome, e-mail, senha, CPF, número e login com autenticação 2FA via authenticator, incluindo bloqueio de acessos com credenciais inválidas e recuperação de senha. |
| **M** | 100% dos usuários devem conseguir se cadastrar e acessar o sistema. O sistema deve bloquear acessos com credenciais inválidas. |
| **A** | O sistema deve conter front-end estruturado, Django no back-end, PostgreSQL no banco de dados, Django para hash de senhas e rastreamento via server-side tracking para gerenciamento de sessão. |
| **R** | Garantir que apenas usuários autorizados acessem dados pessoais e financeiros, conforme exigido pela LGPD. |
| **T** | Módulo finalizado e testado, iniciando em 5 de junho até 1 de outubro. |

**Descrição:**  
Será desenvolvido um módulo completo para que os afiliados possam criar uma conta no sistema e acessá-la com segurança. O cadastro exigirá nome, e-mail, senha, CPF e número. O login será feito com e-mail ou número e senha, com proteção contra múltiplas tentativas inválidas e 2FA via authenticator. O sistema utilizará server-side tracking para gerenciar sessões de forma segura.

---

### Objetivo 2 – Cadastro e Rastreamento de Links

| Critério | Descrição |
|----------|-----------|
| **S** | Desenvolver módulo para o afiliado cadastrar, editar e excluir links de produtos, com rastreamento de cliques e conversões. |
| **M** | O sistema deve registrar 100% dos cliques, armazenar data/hora, IP e origem do clique. Deve gerar relatórios de cliques por período. |
| **A** | Utilizar server-side tracking para evitar bloqueios de navegadores. Gerar links únicos com parâmetros automaticamente. |
| **R** | Fornecer dados precisos para cálculo de comissões e taxa de conversão (vendas / cliques). |
| **T** | 1 de outubro até 1 de novembro. |

**Descrição:**  
Será desenvolvido um módulo completo para que o afiliado possa gerenciar seus links de produtos de forma centralizada. O sistema permitirá cadastrar, editar e excluir links, associando cada um a um produto, categoria ou marketplace específico. Cada link cadastrado receberá automaticamente um identificador único para rastreamento preciso. Sempre que um usuário final clicar no link, o sistema registrará a data/hora, o endereço de IP, o navegador (user-agent) e a origem do clique (referer). O rastreamento será feito via server-side tracking, processando os dados diretamente no servidor para evitar bloqueios por adblocks ou navegadores. O sistema também capturará conversões (vendas realizadas) via integração com API do produtor/plataforma de afiliados. Com base nos dados coletados, o sistema gerará relatórios gráficos de cliques por período (diário, semanal, mensal) e calculará automaticamente a taxa de conversão (vendas / cliques), fornecendo insumos precisos para o cálculo de comissões.

