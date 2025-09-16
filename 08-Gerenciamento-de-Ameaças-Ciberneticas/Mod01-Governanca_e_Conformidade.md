# Módulo 1 - Governança e Conformidade


### Síntese
```
Neste módulo, tivemos uma introdução à base estratégica da cibersegurança, focando nos conceitos de Governança, Risco e Conformidade (GRC).
Aprendemos como as organizações avaliam riscos de forma qualitativa, usando níveis como 'alto' e 'baixo', e a importância de priorizar os ativos mais críticos para o negócio antes de qualquer ação técnica. Vimos também como a Análise de Impacto Empresarial (BIA) é fundamental para definir métricas de recuperação, como o RTO e o RPO
Discutimos o papel das políticas de segurança, que alinham as ações com a missão da empresa, e como diferentes funções de administração de dados (Data Owner, Custodian, etc.) são responsáveis por proteger as informações. Finalmente, exploramos como frameworks importantes como o CIS Controls e leis como a CFAA fornecem as diretrizes e regras para que os profissionais atuem de forma ética e eficaz.
```
---

## 1.1 - Governança

- É o conjunto de regras que define quem toma as decisões sobre os riscos de segurança em uma empresa. Ela estabelece a responsabilidade e garante que as estratégias de segurança estejam alinhadas com os objetivos do negócio e com as leis.
- A principal diferença entre **Governança** e **Gerenciamento** é que a *Governança* define a estratégia e a responsabilidade `('o quê' e o 'porquê')`. O *Gerenciamento* implementa os controles técnicos para executar essa estratégia `(o 'como')`.

#### Papeis importantes

- **Proprietário dos Dados (Data Owner):** Geralmente um gerente ou diretor. Ele é o responsável final pelo dado. Decide quem pode acessá-lo e qual sua classificação (ex: público, interno, confidencial).
- **Controlador dos Dados (Data Controller):** Define a finalidade e a maneira como os dados pessoais são processados. Está muito ligado a leis de privacidade como a LGPD.
- **Custodiante de Dados (Data Custodian):** A equipe de TI. É quem implementa os controles técnicos definidos pelo Propietário. Ex: configura as permissões em um banco de dados.
- **Processador de Dados (Data Processor):** Uma empresa terceira que processa dados em nome da sua empresa (ex: um serviço de nuvem como a AWS).
- **Oficial de Proteção de Dados (DPO):** O especialista que garante que a empresa esteja em conformidade com as leis de proteção de dados.

#### Políticas de Segurança Cibernética

- São documentos de alto nível que descrevem a visão, as metas e as responsabilidades de segurança de uma empresa. São a "constituição" da segurança da informação.
- **Por que são importantes:** Demonstram o compromisso da empresa, definem regras claras para todos os funcionários, garantem consistência e dão à equipe de segurança o apoio da alta gerência para agir.

#### Tipos Comuns de Políticas de Segurança

1. **Política de Utilização Aceitável (AUP):** Define o que os funcionários podem e não podem fazer com os recursos da empresa (Internet, computadores, etc.).
2. **Política de Senhas:** Define as regras para a criação de senhas (tamanho mínimo, complexidade, frequência de troca).
3. **Política de Acesso Remoto:** Define as regras para se conectar à rede da empresa de fora (ex: uso obrigatório de VPN).
4. **Política de Tratamento de Incidentes:** Um guia passo a passo sobre o que fazer quando um incidente de segurança (como um vazamento de dados) acontece.
- Como desenvolvedor, você frequentemente terá que consultar a "*Política de Utilização Aceitável*" para saber se pode instalar uma nova ferramenta, e a "*Política de Senhas*" para garantir que suas aplicações sigam as regras da empresa.

---

## 1.2 - A Ética da Segurança Cibernética

- É a 'bússola moral' do profissional. É o conjunto de princípios que te guia a tomar as decisões corretas, diferenciando o uso do seu conhecimenot técnico para o bem (*hacker ético*) e para o mal (*Cibercriminoso*).
- **Abordagens Éticas:**
    - **Utilitarista:** A ação correta é a que traz o maior bem para o maior número de pessoas.
    - **Abordagem de Direitos:** As ações devem respeitar os direitos fundamentais dos indivíduos (privacidade, segurança, etc.).
    - **Abordagem de Bem Comum:** As ações devem beneficiar a comunidade como um todo.

    O *Computer Ethics Institute* criou '**Os 10 Mandamentos da Ética em Computadores**', que são um excelente guia prático, como por exemplo: *`Não usarás o computador para prejudicar outras pessoas`* e o *`Não usarás os recursos de computadores de outras pessoas sem autorização`*.

#### Cibercrime e Leis Cibernéticas

- **Tipos de Cibercrime:**
    - **Crime por Computador:** O computador é o *alvo* (ex: Infecção por malware, invasão).
    - **Crime Assistido por Computador:** O computador é a *ferramenta* (ex: Fraude online, roubo de identidade).
- **Leis Cibernéticas:**
    - O maior desafio é que a tecnologia e o cibercrime evoluem muito mais rápido do que a capacidade dos sitemas legais de criar leis.
    - **Legislação (exemplo dos EUA):** Existem leis para diferentes níveis:
        - **Estaturárias:** Criadas pelo congresso, com penas criminais.
        - **Administrativas:** Regras de agências do governo.
        - **Direito Comum:** Baseada em decisões judiciais anteriores.
    - **Leis Específicas:** Existem leis e padrões para setores específicos, como:
        - **Financeiro (GLBA):** Controla como as informações financeiras dos clientes são usadas e compartilhadas.
        - **Contabilidade (SOX):** Regula as práticas financeiras de empresas de capital aberto.
        - **Cartão de Crédito (PCI DSS):** Um conjunto de regras para proteger os dados de cartões de pagamento durante transações. Embora 'voluntário', não seguir o PCI DSS pode resultar em multas pesadas.
    - **Leis de Privacidade:** Exigem que empresas notifiquem os clientes em caso de vazamento de dados (violação). Nos EUA, a califórnia foi pioneira com a lei SB 1386.
    - **Internacional:** *A Convenção Sobre o Crime Digital* (Convenção de Budapeste) é o principal tratado internacional para harmonizar as leis e facilitar a cooperação entre países.

No Brasil, a lei mais importante que você deve conhecer sobre privacidade é **a LGPD (Lei Geral de Protenção de Dados)**, que é fortemente inspirada na **GDPR europeia** e regula como empresas coletam, usam e protegem os dados pessoais dos cidadãos.

---

## 1.3 - Estruturas de Gerenciamento de Segurança

#### ISO / IEC 27000

- **O que é:** Uma família de padrões internacionais (uma 'biblioteca') para o gerenciamento da segurança a informação. São as melhores práticas reconhecidas mundialmente.
- **ISMS (Information Security Management System):** É o 'coração' da ISO 27000. Consiste em todos os controles (administrativos, técnicos, operacionais) que uma empresa implementa para manter a informação segura.
- **Os 12 Domínios:** A estrtura da ISO / IEC é dividida em 12 áreas principais (domínios) que cobrem tudo, desde a 'Avaliação de Risco' e 'Controle de Acesso' ate a 'Segurança Física e Ambiental' e 'Gerenciamento de Continuidade de Negócios'. É um guia completo para não esquecer de nenhuma área importante.

#### Objetivos de Controle e Controles (ISO 27001 vs. ISO 27002)

- **Objetivos de Controle (ISO 27001):** Definem o *'O QUÊ?'*. São os requisitos de alto nível que uma empresa precisa cumprir. Ex: "Garantir que apenas usuários autorizados acessem as informações.".
- **Controles (ISO 27002):** Definem o *'COMO?'*. São as diretrizes e sugestões de como atingir os objetivos. Ex: "Implementar uma política de senhas fortes, usar autenticação de dois fatores, etc.".

Uma empresa **se certifica na ISO 27001** (provando que cumpre os objetivos). Ela **usa a ISO 27002** como um guia para escolher os melhores controles para o seu ambiente.

#### Estados dos Dados e a Tríade CIA

- **Tríade CIA:** A segurança da informação sempre busca proteger três pilares: **C**onfidencialidade, **I**ntegridade, e **D**isponibilidade. A ISO 27000 ajuda a empresa a aplicar controles para proteger esses três pilares.
- **Estados dos Dados:** Os controles devem ser aplicados em todos os três estados em que os dados podem se encontrar:
    - **Em Repouso (in Rest):** Quando os dados estão armazenados (ex: em um SSD, banco de dados).
    - **Em Trânsito (in Transit):** Quando os dados estão viajando pela rede (ex: em um e-mail, acessando um site).
    - **Em Processo (in Use):** Quando os dados estão sendo ativamente usados pela memória RAM e CPU.

#### Outros Frameworks Importantes

- **NIST Cybersecurity Workforce Framework:** Criado pelo NIST (Instituto Nacional de Padrões e Tecnologia dos EUA), ele organiza o trabalho de segurança em 7 categorias (Proteger e Defender, Investigar, Analisar, etc.), definindo as habilidades necessárias para cada função.
- **CIS Controls (Center for Internet Security):** Um conjunto de ações de defesa priorizadas (controles) para ajudar as empresas a se protegerem contra os ataques mais comuns. São considerados mais 'práticos' e 'direto ao ponto' que a ISO.
- **CSA Cloud Controls Matrix (CCM):** Um framework focado especificamente em segurança para computação em nuvem, mapeando controles para os principais padrões e regulamentações do setor.
