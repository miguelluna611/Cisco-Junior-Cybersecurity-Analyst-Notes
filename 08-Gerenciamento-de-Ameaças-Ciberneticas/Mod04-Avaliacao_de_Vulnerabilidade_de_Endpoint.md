# Módulo 04 - Avaliação de Vulnerabilidade de Endpoint

### Síntese

```
Neste módulo 4, eu aprendi sobre o processo completo de Avaliação de Vulnerabilidades, desde a criação de uma linha de base até o gerenciamento contínuo dos riscos.
Eu vi a importância de criar perfis de rede e de servidores, que funcionam como uma "fotografia" do estado normal de operação, para então poder detectar anomalias que podem indicar um ataque. O ponto central foi entender o CVSS (Common Vulnerability Scoring System), o padrão universal que eu posso usar para dar uma nota de 0 a 10 para a gravidade de uma vulnerabilidade, me ajudando a priorizar o que precisa ser corrigido com mais urgência.
Por fim, conectei tudo isso aos processos de gestão contínua, aprendendo as diferentes estratégias de Gerenciamento de Risco (como aceitar, mitigar ou transferir) e o ciclo de vida do Gerenciamento de Vulnerabilidades, onde o Gerenciamento de Patches se destaca como a forma mais eficaz de mitigar as falhas de software encontradas.
```

---

#### Perfilamento (Profiling) de Rede e Servidor

- É o processo de criar uma linha de base (baseline), ou seja, um registro detalhado de como a rede e os sevidores se comportam em condições normais de operação.
- **O que é medido:**
    - **Perfil de Rede:** Quais portas são usadas, qual o volume de tráfego, de onde e para onde os dados fluem, comportamento dos usuários.
    - **Perfil de Servidor:** Uso de CPU, memória, processos em execução, conexões ativas.
- A linha de base serve como  um ponto de referência. Qualquer desvio significativo (anomalias) dessa linha de base pode indicar um problema de segurança, como uma infecção por malware ou um acesso não autorizado.
- **NBA (Network Behavior Analysis):** É a técnica de usar Big Data e Machine Learning para analisar os dados da rede e detectar essas anomalias automaticamente.

#### CVSS (Common Vulnerability Scoring System)

- É um padrão aberto e universal para calcular uma pontuação numérica que representa a gravidade de uma vulnerabilidade de segurança. A pontuação vai de 0.0 a 10.0.
- O objetivo é ajudar as empresas a priorizar quais vulnerabilidades devem ser corrigidas primeiro. Uma falha com nota 9.8 (Crítica) é muito mais urgente que uma com nota 3.5 (Baixa).
- A pontuação é calculada com base em três grupos:
    - **Métricas de Base:** Características intrínsecas da falha (Ex: Vetor de Ataque, Complexidade, Privilégios Necessários). Essa pontuação não muda.
    - **Métricas Temporais:** Fatores que mudam com o tempo (ex: Já existe um exploit disponível? Há uma correção oficial?).
    - **Métricas Ambientais:** Fatores específicos do ambiente da empresa (ex: O sistema afetado é crítico para o negócio).
O CVSS funciona em conjunto com o **CVE**. O CVE dá o 'nome' (o RG) da vulnerabilidade, e o CVSS dá a 'nota' de gravidade para ela.

#### Gerenciamento de Riscos

- É um processo contínuo para identificar, avaliar e tratar os riscos de segurança.
- **Possíveis Respostas a um Risco:**
    - **Retenção (Aceitação):** Aceitar o risco e suas consequências (geralmente quando o custo da correção é maior que o da perda).
    - **Redução (Mitigação):** Tomar medidas para reduzir a vulnerabilidade (ex: aplicar um patch).
    - **Compartilhamento (Transferência):** Terceirizar o risco (ex: contratar um seguro cibernético).
    - **Prevenção (Evitar):** Interromper a atividade que está causando o risco.

#### Processos de Gerenciamento Contínuo

- O **Gerenciamento de Vulnerabilidades** é o ciclo de vida completo para lidar com falhas: `Descobrir > Priorizar Ativos > Avaliar (scan) > Relatar > Remediar (corrigir) > Verificar`.
- Já o **Gerenciamento de Ativos** mantém um inventário de todo o hardware e software da rede para saber o que precisa ser protegido.
- O **Gerenciamento de Configuração** cria 'imagens' e configurações padrão seguras para todos os dispositivos, garantindo a consistência e reduzindo a superfície de ataque.
- Por último, temos o **Gerenciamento de Patches**, com o processo de identificar, testar e aplicar atualizações (patches) de segurança. É a forma mais eficaz de mitigar vulnerabilidades de software.
