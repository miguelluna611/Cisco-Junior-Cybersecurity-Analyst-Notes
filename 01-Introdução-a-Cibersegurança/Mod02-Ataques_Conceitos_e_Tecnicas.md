# Módulo 02 - Ataques, Conceitos e Técnicas

### Síntese

```
Neste módulo, eu aprendi sobre as principais ferramentas e táticas que os cibercriminosos usam para atacar sistemas. Explorei os diferentes tipos de Malware, entendendo a diferença entre um Vírus (que precisa de um hospedeiro), um Worm (que se replica sozinho pela rede) e um Cavalo de Troia (que se disfarça de programa legítimo). Também vi como funcionam malwares como Spyware, Adware e o perigoso Ransomware.
Estudei os métodos de infiltração, com destaque para a Engenharia Social, que manipula pessoas para obter acesso. Vi como funcionam os ataques de Negação de Serviço (DoS e DDoS), que visam derrubar um serviço, e os ataques On-Path (Man-in-the-Middle), que interceptam a comunicação para roubar dados.
Por fim, analisei o conceito de vulnerabilidades, que são as falhas de hardware ou software que os atacantes exploram. Entendi a diferença entre uma vulnerabilidade e um exploit (o código que se aproveita da falha), e vi categorias comuns de falhas de software, como o Buffer Overflow.
```

### Malware

- É qualquer código ou software criado com a intenção de **roubar dados, causar danos ou comprometer um sistema**.
- **Tipos Principais:**
    - **Vírus:** Código malicioso que se anexa a um arquivo executável e precisa da ação do usuário para se espalhar.
    - **Worm:** Similar a um vírus, mas se replica e se espalha pela rede de forma autônoma, sem precisar de um arquivo hospedeiro ou ação do usuário.
    - **Cavalo de Troia (Trojan):** Disfarça-se de software legítimo para enganar o usuário e abrir uma porta de entrada (backdoor) no sistema.
    - **Spyware:** Espiona a atividade do usuário, registrando o que é digitado (leylogger) e capturando dados sensíveis.
    - **Adware:** Exibe anúncios indesejados e pop-ups, geralmente coletando dados de navegação.
    - **Ransomware:** O "sequestrador digital". Criptograda os arquivos e exige um pagamento para liberá-los.
    - **Rootkit:** Malware avançado que se esconde profundamente no sistema operacional para garantir acesso persistente e evitar detecção.
    - **Backdoor:** Um método para contornar a autenticação normal e garantir acesso remoto e não autorizado a um sistema.
    - **Scareware:** Usa táticas de medo (ex: falsos alertas de vírus) para coagir o usuário e instalar mais malware.

### Métodos de Infiltração

- **Engenharia Social:** A arte de manipular pessoas para que elas executem ações ou divulguem informações confidenciais. É o vetor de ataque mais comum e eficaz.
    - **Pretexting:** Criar um cenário ou uma história falsa (pretexto) para enganar a vítima.
- **Negação de Serviço:**
    - **DoS:** Um único atacante inunda um alvo com tráfego para sobrecarregá-lo e torná-lo indisponível.
    - **DDoS:** Um ataque muito mais poderoso, onde o tráfego vem de múltiplas fontes coordenadas (uma **botnet** de computadores 'zumbis').
- **Ataques On-Path (Man-in-the-Middle - MitM):**
    - O atacante se posiciona **entre** a vítima e o servidor (ex: em uma rede Wi-Fi pública), interceptando e podendo até modificar toda a comunicação sem que eles percebam.
- **SEO Poisoning:**
    - Técnica que usa otimização de busca para posicionar sites maliciosos no topo dos resultados do Google, enganando os usuários para que cliquem e se infectem.
- **Ataques de Senha:**
    - **Força Bruta:** Tentar todas as combinações possíveis.
    - **Dicionário:** Tentar uma lista de palavras ou senhas comuns.
    - **Password Spraying:** Tentar uma única senha comum contra uma lista enorme de usuários.
    - **Tabela Rainbow:** Usar tabelas de hashes pré-calculados para descobrir senhas a partir de vazamentos de bancos de dados.

### Vulnerabilidades e Exploits

- **Vulnerabilidade:** É a falha de segurança em um software ou hardware.
- **Exploit:** É o código ou técnica que um atacante usa para se aproveitar de uma vulnerabilidade específica.
- **Categorias Comuns de Vulnerabilidades de Software:**
    - **Buffer Overflow:** Ocorre quando um programa tenta escrever mais dados em uma área de memória (buffer) do que ela comporta, sobrescrevendo áreas adjascentes e permitindo a execução de código malicioso.
    - **Entrada Não Validada:** O programa não verifica corretamente os dados que recebe do usuário, permitindo que entradas maliciosas causem comportamentos inesperados (ex: injeção de SQL).
    - **Condição de Corrida (Race Condition):** Uma falha que ocorre quando a segurança de uma operação depende da ordem ou do tempo de certos eventos, e um atacante consegue interferir nessa sequência.

