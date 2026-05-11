# Análise de viabilidade.

## Introdução:

Análise de viabilidade é o estudo que permite avaliar se um projeto é viável ou não,
nesse estudo olhamos para o projeto de todas as formas possíveis, assim conseguimos prever 
prováveis problemas futuros e pensar em soluções adequadas.

Esse estudo, permite alinhar o pensamento da empresa para que a ideia seja mais realista e adaptada ao ambiente,
ainda que a ideia seja boa, precisamos compreender diversos fatores antes de começar o desenvolvimento, tais como:
gestão da equipe, tecnologias, leis e diretrizes, futuras manutenções, custos entre outros. 
Essa análise se divide principalmente em:
viabilidade técnica, financeira, operacional, legal e comercial.

Este estudo se torna de extrema importância para o projeto Afillimetrics, uma vez que o foco da empresa é o mercado financeiro,
nesse meio, precisamos adquirir a confiança do cliente, para que ele possa perder o medo de aplicar o dinheiro dele na nossa plataforma.
Portanto, teremos que suprir as fraquezas dos nossos concorrentes, fazendo com que clientes migrem para o nosso sistema e atraindo, 
também, pessoas de fora do mercado.

---

## Viabilidade ecônomica:

| ITEM | DESCRIÇÃO | CUSTO ESTIMADO (R$) | BENEFÍCIO ESPERADO |
| :---: | :---: | :---: | :---: |
| **Hardware** | Computadores e domínio próprio. | 50,00 | Economia, através de computadores próprios e acadêmicos, porém com domínio próprio. |
| **Software** | Licenças de IDEs, banco de dados e hospedagem | 60,00 | Economia com uso de tecnologias open-source, porém segurança com uma hospedagem barata e segura. |
| **Mão de obra** | Horas de desenvolvimento e design | Voluntário | Entrega do sistema funcional e aprendizado. |
| **Treinamento** | Treinamento da equipe e capacitação do usuário final. | 200,00 | Desenvolvimento da equipe através de cursos, e criação de guias (voluntário). |
| **Manutenção** | Atualizações e suporte pós-implantação | 800,00 | Infraestrutura escalável, segurança e backups, monitoramento e logs. |
| **Total de Custos** | | **1.150,00** | |

## Conclusão Viabilidade Ecônomica:

Como custo inicial, focamos apenas no necessário, que seria a inclusão de domínio próprio, hospedagem e cursos para aprendizado.
Com isso conseguimos um projeto estável, investindo apenas o nosso tempo com a mão de obra voluntária, e economicamente falando, os gastos seriam quase nulos.
Pórem temos total ciência de que esse projeto não aguentaria uma alta demanda de clientes, por isso o gasto maior seriam as atualizações, 
considerando que estaremos tratando de dados sensíveis e econômicos do consumidor. 

A princípio não pretendemos aplicar todo o dinheiro que foi estimado na tabela, 
a empresa acredita que, com a infraestrutura e segurança que está sendo implementada inicialmente (HTTPS e hashing de senhas), 
seria seguro manter até 20 usuários pagantes, após esse marco, o investimento previsto na tabela seria aplicado. 
Isso justifica o valor que foi estimado, pois com um valor simbólico de R$50,00 para cada usuário, o dinheiro já seria arrecadado pela própria plataforma. 
E o mesmo se torna totalmente compreensível, já que nosso sistema juntamente a um afiliado disposto a analisar o mercado, 
arrecadaria um ROI maior do que o valor cobrado pelos nossos serviços.

---

## Viabilidade Técnica:

| REQUISITO TÉCNICO | DESCRIÇÃO | DISPONIBILIDADE | OBSERVAÇÕES |
| :---: | :---: | :---: | :---: |
| **Linguagem de Programação** | Python, JavaScript | Parcial | Necessário revisão de linguagens. |
| **Frameworks** | Django | Parcial | Equipe em treinamento de framework. |
| **Banco de Dados** | MySQL | Sim | Gratuito e compatível com o projeto. |
| **Infraestrutura** | Hospedagem em nuvem | Parcial | Hospedagem em nuvem com baixo custo (Equipe precisa de treinamento). |
| **Ferramentas de Desenvolvimento** | IDE (Visual Studio Code) | Sim | Ferramenta gratuita. |
| **Equipe Técnica** | Desenvolvedores, analistas, designers | Sim | Equipe reduzida, porém qualificados. |
| **Compatibilidade** | Suporte a dispositivos móveis e desktop | Sim | Testes planejados em múltiplas plataformas (apenas web). |
| **Segurança** | Autenticação, criptografia (HTTPS/Hash) e 2FA (Authenticator). | Parcial | Equipe em aprendizado de protocolos padrão de segurança. |

## Conclusão da Viabilidade Técnica:

Para criação do projeto, está totalmente definido quais ferramentas serão utilizadas, e ciência de como as mesmas funcionam.
Pórem, não é de total conhecimento do grupo, como desenvolver certos recursos em ferramentas específicas (implementação em Django, 
configuração de hospedagem em nuvem e protocolos de segurança do projeto).
Pretendemos nesse primeiro momento entender completamente o que de fato será utilizado no desenvolvimento, desse modo, na fase de programação,
teremos clareza no que foi estudado, evitando desperdicio de tempo com tecnologias que não serão implementadas.

---

## Viabilidade Operacional:

| ASPECTO OPERACIONAL | DESCRIÇÃO | SITUAÇÃO ATUAL | OBSERVAÇÕES |
| :---: | :---: | :---: | :---: |
| **Perfil dos Usuários** | Pequenos ou novos afiliados. | Definido | Usuários já familiarizados com tecnologia, mas não tanto com o mercado. |
| **Treinamento Necessário** | Capacitação para uso do sistema. | Baixa | Necessário apenas para novos afiliados. |
| **Adaptação ao Fluxo de Trabalho** | Junção de processos existentes, tornando-os mais simples. | Baixa | Reconstruir modo de trabalho baseado em perfil do cliente. |
| **Facilidade de Uso (UX/UI)** | Interface intuitiva e acessível. | Médio | Interfaces intuitivas planejadas. |
| **Resistência à Mudança** | Aceitação dos usuários em migrar para o novo sistema. | Alto | Necessário marketing estratégico expondo oportunidade de nova renda. |
| **Suporte e Manutenção** | Disponibilidade de suporte técnico. | Médio | Equipe interna em treinamento para suporte. |
| **Impacto na Produtividade** | Redução de ambientes, aumento no ROI. | Alto | Redução de tempo em trocas de ambientes, e diminuição de perdas de clientes com remarketing. |

## Conclusão da Viabilidade operacional: 

Pretendemos criar um sistema para reunir e simplificar tudo que um afiliado precisa no mesmo ambiente, portanto, um afiliado, mesmo que iniciante, 
não terá dificuldades para migrar para a nossa plataforma, e aos novos usuários será disponibilizado um treinamento simples para entender melhor termos técnicos do mercado. 
Desse modo, conseguimos criar nosso sistema por completo partindo do pensamento que todos os usuários terão conhecimento básico sobre como ser um afiliado.

Está sendo desenvolvida uma interface intuitiva e focada em gráficos, os mesmos que serão gerados a partir de metas do próprio cliente,
desse modo ajudamos a visualização e o entendimento rápido do usuário baseado em seus objetivos.

---

### Viabilidade Legal

| ASPECTO LEGAL | DESCRIÇÃO | SITUAÇÃO ATUAL | OBSERVAÇÕES |
| :---: | :---: | :---: | :---: |
| **Proteção de Dados (LGPD)** | Conformidade com a Lei Geral de Proteção de Dados. | Parcial | Foco em transparência e acesso restrito aos dados financeiros. |
| **Direitos Autorais** | Uso de imagens de terceiros. | Parcial | Cuidado com direitos de imagens. |
| **Licenciamento de Software** | Ferramentas e bibliotecas utilizadas. | Sim | Uso de tecnologias open source (Django, Python, JavaScript e MySQL). |
| **Normas do Setor** | Regulamentações de marketing e plataformas. | Parcial | Alinhamento com as diretrizes da CONAR e termos de uso das plataformas de afiliados. |
| **Termos de Uso** | Contrato de serviços com usuário. | Sim | Definição de métodos e limites da plataforma e do suporte. |
| **Segurança da Informação** | Implementação de autenticação e criptografia. | Sim | Uso de protocolos HTTPS, Hash de senhas e 2FA (Authenticator). |

## Conclusão da Viabilidade Legal:

O sistema depende de diversos dados sensíveis do usuário, e também envolve a exibição de produtos de terceiros dentro da plataforma, por isso tomamos o cuidado de informar detalhadamente os limites e intuito do sistema através dos termos de uso.
Esclarecendo que não garantimos lucros, apenas fornecemos auxílio para que um afiliado utilize melhor seu tempo e entenda perfeitamente onde está sendo investido seu dinheiro.
Irá conter também uso de modelos prontos feitos por designers qualificados para isso, pórem, apenas a estrutura visual será de responsabilidade da empresa, qualquer objeto editável ficará sob encargo do cliente.


