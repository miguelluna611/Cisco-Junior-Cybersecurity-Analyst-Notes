# Módulo 3 - Inteligência de Ameaças

### Síntese

```
Neste módulo, eu mergulhei no conceito de Inteligência de Ameaças (Threat Intelligence), entendendo que é a prática de coletar e analisar informações para compreender as ameaças e agir de forma proativa.
Eu vi que os profissionais de segurança se mantêm atualizados através de diversas fontes, como relatórios da Cisco, publicações de organizações respeitadas como a SANS e alertas do CIS. Aprendi sobre as grandes equipes de inteligência, como o Cisco Talos, que pesquisam e combatem ameaças ativas em tempo real.
O mais importante foi entender como essa informação é organizada: eu aprendi sobre o sistema CVE, que funciona como um "RG" para cada vulnerabilidade conhecida, e sobre como governos e empresas compartilham indicadores de ameaças automaticamente através de serviços como o AIS. Por fim, eu vi que toda essa inteligência é consolidada em Plataformas de Inteligência de Ameaças (TIPs) para facilitar a análise e a tomada de decisão.
```

---

#### Fontes de Informação de Segurança

- São os canais onde os profissionais se mantêm atualizados sobre as novas ameaças, vulnerabilidades e técnicas de defesa.
- **Tipos de Fontes:**
    - **Organização:** SANS Institute, FIRST, (ISC)², etc., que fornecem pesquisas, treinamentos e alertas.
    - **Relatórios Corporativos:** Grandes empresas de segurança, como a Cisco, publicam relatórios anuais e semestrais com análises de tendências e estatísticas de ataques.
    - **Mídia Especializada:** Blogs e podcasts de segurança são essenciais para notícias diárias e discussões sobre novas técnicas.

#### Serviços e Padrões de Inteligência de Ameaças

- São serviõs e tecnologias que coletam, processam e distribuem informações sobre ameaças de forma estruturada e, muitas vezes, automatizada.
- **Exemplos de Serviços:**
    - **Cisco Talos:** Uma das maiores equipes comerciais de inteligência de ameaças do mundo. Eles pesquisam e descobrem ameaças ativas e fornecem proteçaõ para os produtos da Cisco.
    - **FireEye:** Outra grande empresa do setor que combina tecnologia com especialistas humanos para fornecer serviços de proteção e inteligência.
    - **AIS (Automated Indicator Sharing):** Um serviço gratuito do governo dos EUA que permite a troca de "Indicadores de Comprometimento" (IOCs) em tempo real entre o governo e empresas privadas. Um IOC pode ser um endereço de IP malicioso, um domínio de phishing, etc.
- **CVE (Common Vulnerabilities and Exposures):**
    - É um dicionário ou um 'RG' para cada vulnerabilidade de segurança publicamente conhecida. É mantido pela MITRE Corporation com patrocínio do governo dos EUA.
    - Cada vulnerabilidade recebe um identificador único (*ex: CVE-2024-12345*), permitindo que todos na indústria (fabricantes de software, pesquisadores, scanners) se refiram ao mesmo problema de forma inequívoca.
    ```
    Quando um scanner de vulnerabilidades como o Nessus encontra uma falha, ele geralmente informa o código CVE correspondente. Saber pesquisar por um CVE é uma habilidade fundamental.
- **Padrões de Comunicação (Ex: STIX/TAXII):**
    - São a 'linguagem' (STIX) e o 'protocolo de transporte' (TAXII) que as máquinas usam para trocar informações de inteligência de ameaças de forma automatizada.
- **TIPs (Threat Intelligence Platforms):**
    - São 'Centrais de Comando' que agregam informações de múltiplas fontes (feeds de IOCs, relatórios, etc.) em um único lugar, ajudando os analistas a gerenciar e a usar essa inteligência.
