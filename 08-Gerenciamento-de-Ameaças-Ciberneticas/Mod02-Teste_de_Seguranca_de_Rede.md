# Módulo 2 - Teste de Segurança de Rede

### Síntese



---

## 2.1 - Avaliações de Segurança

#### Scanners de Vulnerabilidades

- São programas que automatizam a busca por pontos fracos em computadores, redes ou aplicações. Eles são essenciais para uma auditoria de segurança.
- **O que procuram:**
    - Senhas padrão ou fracas.
    - Softwares e sistemas desatualizados (sem patches de segurança).
    - Portas de rede abertas desnecessariamente.
    - Erros de configuração em sistemas.
- **Exemplos de ferramentas famosas:** Nessus, Core Impact, GFI LanGuard.

#### Tipos de Varreduras (Scans)

- **Scanners de Rede:** Investigam a rede em busca de hosts ativos e potas abertas, tentando identificar serviços vulneráveis.
- **Scanners de Aplicação:** Testam o código-fonte de uma aplicação "de dentro para fora", procurando por falhas de programação.
- **Scanners de Aplicação Web:** Focados em encontrar vulnerabilidades específicas de sites e sustenas web (como as da OWASP Top 10).

#### Ferramentas de Diagnóstico

- Comandos essenciais para fazer uma verificação manual e rápida da rede. São o "canivete suíço" do analista.
- **Exemplos:**
    - *ping*: Testar conectividade;
    - *arp*: Ver dispositivos na rede local;
    - *nslookup*: Consultar DNS;
    - *netstat*: Ver conexões de rede ativas;
    - **nmap**: Mapear redes e portas;

Nos estudos são mencionados os comandos `ipconfig` e `tracert`, que são comandos do Windows. No Linux, os equivalentes usados são `ip a` (ou `iopconfig`) e `traceroute`.

#### Automação de Segurança: SIEM vs. SOAR

Essa é uma dupla fundamental na segurança moderna.

- **SIEM (Security Information and Event Management)**
    - **Função Principal:** **AGREGAR** e **ANALISAR**. É a grande "central de monitoramento".
    - Coleta logs (*registros de eventos*) de todas as fontes possíveis (firewalls, servidores, notebooks) em um único lugar. Ele ua inteligência para correlacionar eventos, encontrar anomalias e gerar alertas sobre atividades suspeitas.
    - É como um sistema de câmeras e sensores de alarme de um shopping. Ele observa tudo e dispara um alarme se vir algo estranho.

- **SOAR (Security Orchestration, Automation, and Response)**
    - **Função Principal:** **AGIR** e **AUTOMATIZAR**. É a equipe de resposta rápida automatizada.
    - Ele **recebe os alertas do SIEM** e, com base em regras pré-definidas (*playbooks*), toma ações automáticas para conter a ameaça.
    - E se o SIEM é o sistema que dispara o alarme de incêndio, o SOAR é o sistema que, ao receber o alarme, automaticamente tranca as portas corta-fogo, aciona os sprinkles e liga para os bombeiros, tudo sem intervenção humana.

---

## 2.2 - Técnicas de Teste de Segurança de Rede

#### Segurança das Operações (OPSEC)

- Refere-se às práticas diárias e contínuas para manter uma rede segura, desde o planejamento inicial até a manutenção constante. Não adianta ter a melhor tecnologia se as operações do dia a dia forem inseguras.
- **Conhecimentos Necessários:** Um profissional que realiza testes precisa ter uma base sólida em sistemas operacionais, redes (TCP/IP), hardening (enrijecimento de sistemas) e ferramentas como firewalls e IPSs (Sistemas de Prevenção de Intrusão).

#### Teste de Avaliação de Segurança (ST&E)

- Um exame formal e completo das medidas de proteção de uma rede que já está em funcionamento. É como uma 'vistoria' completa do sistema para garantir que tudo está operando como deveria.
- **Objetivos Principais:**
    - Encontrar falhas de design ou implementações que violem as políticas de segurança.
    - Verificar se os mecanismos de segurança (firewalls, etc.) são adequados.
    - Garantir que a documentação do sistema corresponde à realidade.
- Deve ser feito periodicamente e, obrigatoriamente, sempre que uma mudança significativa for feita na rede.

#### Tipos de Testes de Rede

- **Teste de Penetração (Pentest):**
    - Simula um ataque real de uma fonte maliciosa para ver se é possível invadir o sistema e quais seriam as consequências. Pode incluir técnicas de engenharia social (enganar pessoas).
    - É o teste mais ativo e agressivo.
- **Varredura de Rede (Network Scanning):**
    - Mapeia a rede para descobrir quais computadores estão ativos, quais portas estão abertas e quais serviços estão rodando neles (ex: um servidor web, um banco de dados).
    - A ferramenta clássica é o **Nmap**.
- **Varredura de Vulnerabilidade (Vulnerability Scanning):**
    - Usa ferramentas automatizadas (scanners) para procurar por fraquezas conhecidas, como softwares desatualizados, senhas padrão e erros de configuração.
- **Quebra de Senhas (Password Cracking):**
    - Tenta descobrir senhas fracas no sistema, geralmente testando listas de senhas comuns ou usando força bruta, para forçar a implementação de políticas de senhas mais fortes.
- **Revisão de Logs:**
    - Analisa os registros (logs) gerados por servidores, firewalls e outros sistemas em busca de atividades anormais ou suspeitas que possam indicar um ataque.
- **Verificadores de Integridade (File Integrity Monitoring - FIM):**
    - Monitora arquivos críticos do sistema e alerta se algum deles for modificado sem autorização. É uma forma de detectar se um invasor alterou algo no sistema.
- **Detecção de Vírus (Antimalware):**
    - O uso de software antivírus/antimalware para escanear e remover códigos maliciosos.

#### Utilidade dos Resultados

Os resultados de todos esses testes não servem apenas para encontrar problemas. Eles são usados de forma estratégica para:
- Definir um plano de ação para corrigir falhas (mitigação);
- Medir o progresso da segurança da organização ao longo do tempo;
- Justificar investimentos em novas ferramentas ou pessoal de segurança;
- Melhorar a avaliação de riscos e o planejamento de continuidade do negócio;

---

## 2.3 - Ferramentas de Teste de Segurança de Rede

#### Ferramentas de Teste de Rede

- São softwares, tanto de código aberto quanto comerciais, projetados para realizar os testes de segurança que vimos na aula anterior (varredura de vulnerabilidades, mapeamento de rede, etc.).
- **Objetivo:** Automatizar e facilitar a descoberta de fraquezas em uma rede ou sistema.

#### As ferramentas e Suas Funções Principais

- **Nmap / Zenmap:**
    - **Função:** Mapeamento de Rede e Descoberta. É a ferramenta principal para reconhecimento.
    - "Desenha" um mapa da rede, descobrindo quais computadores (hosts) estão ativos, quais portas estão abertas e quais serviços (ex: servidor web) estão rodando em cada porta. O Zenmap é apenas a interface gráfica (GUI) do Nmap.
- **SuperScan:**
    - **Função:** Scanner de Portas (focado em Windows).
    - Similar ao Nmap, mas é uma ferramenta específica para o ambiente Windows. Deteca portas TCP/UDP abertas e realiza outras consultas simples de rede (ping, tracerout, etc.).
- **Scanners de Vulnerabilidade (Ex: Nessus, GFI Languard):**
    - **Função:** Identificação de Fraquezas.
    - Vão um passo além do Nmap. Após descobrir os serviços que estão rodando, eles comparam as versões desses serviços com um banco de dados gigantesco de vulnerabilidades conhecidas (CVEs) e alertam sobre falhas de segurança, erros de configuração e a falta de patches.
- **Ferramentas de Auditoria de Senha (Ex: L0phtCrack):**
    - **Função:** Testar a força das senhas.
    - Usam técnicas como ataques de dicionário e força bruta para tentar descobrir senhas de usuários e identificar contas com credenciais fracas.
- **Frameworks de Exploração (Ex: Metasploit):**
    - **Função:** Teste de Invasão (Pentest) e Exploração.
    - É um "canivete suíço" para o pentester. Fornece uma coleção de "exploits" (códigos que exploram vulnerabilidades) prontos para serem usados. Após um scanner como o Nessus encontrar uma falha, o Metasploit pode ser usado para tentar explorar essa falha e ganhar acesso ao sistema.
- **SIEM (Security Information and Event Management):**
    - **Função:** Monitoramento Centralizado e Análise de Eventos.
    - Agrega e correlaciona logs de múltiplas fontes (firewalls, servidores, etc.) para fornecer uma visão em tempo real da segurança da rede, detectar anomalias e auxiliar em investigações forenses.
- **FIM (File Integrity Monitoring) (Ex: Tripwire):**
    - **Função:** Monitoramento de Integridade de Arquivos.
    - Valida as configurações de TI comparando o estado atual dos arquivos do sistema com uma trilha "linha de base" segura e conhecida, alertando sobre qualquer mudança não autorizada.

---

## Módulo 4 - Teste de Penetração (Pentest)

#### Teste de Penetração (Pentest)
- É um método prático para testar a segurança de um sistema, simulando um ataque cibernético real com a permissão do proprietário. Também é conhecido como "hacking ético".
- **Diferença para Varredura de Vulnerabilidades:
    - Uma *Varredura de Vulnerabilidades* apenas **identifica** possíveis problemas (ex: 'há uma janela destrancada).
    - Um *Pentest* tenta ativamente **explorar** esses problemas para ver até onde um invasor conseguiria ir (ex: 'eu não só vi a janela destrancada, como entrei, cheguei no cofre e consegui a senha').
- **Níveis de Teste (Boxes):**
    - **Black Box (Caixa Preta):** O testador não tem nenhuma informação prévia sobre o alvo. Simula um ataque externo real.
    - **White Box (Caixa Branca):** O testador tem acesso total à informação do sistema(código-fonte, diagrama de rede). Simula uma ameaça interna ou uma auditoria profunda.
    - **Gray Box (Caixa Cinza):** Uma mistura dos dois. O testador tem algumas informações, com as de um usuáiro comum, para simular um ataque de um cliente ou funcionário com poucos privilégios.

#### As 4 Fases de um Pentest
- **Fase 1: Planejamento**
    - A fase do contrato. Define o escopo do teste (o que pode e o que não pode ser atacado) e as 'regras de engajamento'.
- **Fase 2: Descoberta (Reconhecimento)**
    - A fase de coleta de informações.
        - **Passiva (Footprinting):** Coletar dados sem interagir com o alvo (ex: pesquisar sobre a empresa, ver perfis de funcionários no LinkedIn).
        - **Ativa:** Interagir diretamente com o alvo para mapear a rede (ex: usar o `Nmap` para escanear portas).
- **Fase 3: Ataque**
    * A execução da invasão. Envolve explorar as vulnerabilidades encontradas na *Fase 2* para ganhar acesso, escalar privilégios (tornar-se administrador), mover-se lateralmente (pular para outras máquinas na rede) e estabelecer persistência (criar uma *backdoor* para voltar depois).
- **Fase 4: Geração de Relatórios**
    - A fase mais importante. O pentester documenta tudo o que foi feito, as falhas encontradas, o risco que elas representam e, principalmente, como corrigi-las.

#### Ferramentas de Análise de Rede

- **Analisador de Pacotes (Packet Analyzer / Sniffer):**
    - Uma ferramenta que intercepta, registra e decodifica todo o tráfego que passa por uma rede.
    - **Funções:**
        - Diagnosticar problemas de rede.
        - Detectar tentativas de invasão.
        - Capturar dados sensíveis (como senhas, se não estiverem criptografados).
    - **Técnica Associada (Sniffing):** É o ato de "farejar" ou "escutar" o tráfego de rede. Um sniffer coloca a placa de rede em "modo promíscuo", fazendo com que ela capture pacotes destinados a outros computadores e não apenas a si mesma.
    - Uma ferramenta clássica pra isso é o **Wireshark**.
