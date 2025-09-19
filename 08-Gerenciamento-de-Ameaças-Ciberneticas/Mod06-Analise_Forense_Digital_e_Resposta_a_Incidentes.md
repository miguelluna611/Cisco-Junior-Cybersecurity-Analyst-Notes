# Módulo 06: Análise Forense Digital e Resposta a Incidentes

### Síntese
```
Neste último módulo, eu aprendi sobre o que fazer quando um ataque realmente acontece. Explorei o universo da Análise Forense Digital, entendendo o processo formal de coletar, examinar, analisar e relatar evidências de um crime cibernético, e aimportância crítica da Cadeia de Custódia para garantir que as provas sejam válidas. Eu vi como a coleta de evidências deve ser priorizada pela volatidade, começando pela memória RAM.
Aprendi também sobre dois frameworks famosos para entender o comportamento de um atacante: a Cyber Kill Chain, que descreve as 7 etapas de uma intrusão, e o Modelo Diamond que analisa um evento de segurança pelos seus quatro componentes (Adversário, Capacidade, Infraestrutura e Vítima).
Por fim, mergulhei nos processos de Resposta a Incidentes, seguindo o padrão do NIST (Preparação, Detecção/Análise, Contenção/Erradicação/Recuperação, Pós-Incidente), e entendi a diferença entre um Plano de Recuperação de Desastres (DRP), que é focado em restaurar a tecnologia, e um Plano de Continuidade de Negócios (BCP), que é mais amplo e visa manter a empresa operando mesmo durante uma crise.
```
---

#### Análise Forense Digital

- A recuperação e investigação de informações encontradas em dispositivos digitais para serem usadas como evidência em casos criminais ou investigações internas.
- **Processo Forense (4 Etapas - NIST):**
    - **Coleta:** Identificar e adquirir os dados de forma segura, sem alterá-los.
    - **Exame:** Extrair as informações relevantes dos dados coletados.
    - **Análise:** Tirar conclusões a partir das informações, correlacionando fatos.
    - **Relatório:** Apresentar as conclusões de forma imparcial.
- **Ordem de Volatilidade:** A coleta de evidências deve sempre começar pelos dados mais voláteis (que se perdem mais facilmente), seguindo a ordem: `Memória RAM > Arquivos Temporários > Discos Rígidos > Backups Arquivados`.
- **Cadeia de Custódia:** Um registro rigoroso de quem manuseou a evidência, quando e onde, para garantir sua integridade e validade legal.

---

#### Frameworks de Análise de Ataques

- **Cyber Kill Chain (Lockheed Martin)** é um modelo que descreve as 7 etapas que um adversário precisa completar para ter sucesso em um ataque. Se a defesa conseguir quebrar a corrente em qualquer uma das etapas, o ataque falha.
    - **As 7 Etapas:** `Reconhecimento > Armamento > Entrega > Exploração > Instalação > Comando e Controle (C2) > Ações nos Objetivos`.
- **Modelo Diamond de Análise de Intrusão** é outro modelo que analisa cada evento de segurança individualmente, com base em quatro componentes principais que formam um "diamante".
    - **Os 4 Componentes:**
        1. **Adversário:** Quem está atacando;
        2. **Capacidade (Capability):** As ferramentas e técnicas usadas (ex: um malware);
        3. **Infraestrutura (Infrastructure):** O caminho usado pelo ataque (ex: um endereço de IP);
        4. **Vítima (Victim):** O alvo do ataque.

--- 

#### Resposta à Incidentes e Recuperação de Desastres

- **Resposta a Incidentes (Padrão NIST 800-61r2):
    - É um conjunto de políticas e procedimentos para responder a um ataque cibernético.
    - **Ciclo de Vida (4 Fases):**
        1. **Preparação:** Treinar a equipe e preparar as ferramentas;
        2. **Detecção e Análise:** Identificar e validar que um incidente ocorreu;
        3. **Contenção, Erradicação e Recuperação:** Isolar o problema, remover a ameaça e restaurar os sistemas;
        4. **Atividades Pós-Incidente:** Documentar o caso, aprender as lições e melhorar as defesas;
    - **CISRT (Computer Security Incident Response Team):** A equipe especializada responsável por executar esse processo.
- **Recuperação de Desastres (DRP) vs. Continuidade de Negócios (BCP):
    - **DRP (Plano de Recuperação de Desastres):** Focado na tecnologia. É o plano para avaliar, reparar e restaurar os sistemas e dados após um desastre (natural ou humano).
    - **BCP (Plano de Coninuidade de Negócios):** Mais amplo e estratégico. Inclui o DRP, mas também considera como manter as operações essenciais da empresa funcionando, mesmo que seja em um local alternativo, envolvendo pessoal, processos e comunicação. A **BIA (Análise de Impacto nos Negócios)** é o primeiro passo para criar um BCP.
---