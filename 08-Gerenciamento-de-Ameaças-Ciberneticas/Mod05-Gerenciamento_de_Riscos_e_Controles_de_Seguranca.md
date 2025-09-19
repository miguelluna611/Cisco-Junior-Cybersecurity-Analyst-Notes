# Módulo 05 - Gerenciamento de Riscos e Controles de Segurança

### Síntese

```
Neste módulo, eu aprendi os processos formais de Gerenciamento de Risco, que é uma atividade contínua para identificar, avaliar e tratar ameaças a um nível aceitável. Eu entendi os diferentes tipos de fontes de ameaças (adversariais, acidentais, estruturais e ambientais) e as duas principais formas de análkise de risco: a quantitativa , que atribui valores monetários (como no cálculo da ALE - Expectativa de Perna Anual), e a qualitativa, que usa matrizes e mapas de calor para priorizar riscos com base na probabilidade e no impacto.
O mais importante foi entender os Controles de Segurança, que são as contramedidas que implementamos. Eu aprendi a classificá-los por tipo (técnico, administrativo, físico) e por função, como os controles preventivos, que impedem incidentes, os de detecção, que identificam incidentes em andamento, e os de recuperação, que restauram o sistema após um incidente.
```

---

#### Gerenciamento de Risco

- Risco é a probabilidade de uma ameaça explorar uma vulnerabilidade e causar uma perda. O objetivo não é eliminar 100% do risco (o que é impossível), mas reduzi-lo a um nível aceitável para o negócio.
- O gerenciamento de risco é um ciclo, um processo contínuo:
    - **Identificar:** Listar todas as possíveis ameaças.
    - **Avaliar/Analisar:** Medir a gravidade e a probabilidade de cada ameaça.
    - **Planejar Resposta:** Decidir o que fazer com cada risco.
    - **Implementar:** Aplicar os controles.
    - **Monitorar:** Revisar continuamente se os controles estão funcionando.
- O documento ou sistema que registra todos os riscos identificados, suas avaliações e as ações tomadas é conhecido por **Registro de Riscos**.

---

#### Avaliação e Análise de Risco

- **Fontes de Ameaças:**
    - **Adversarial:** Ataques intencionais de pessoas ou grupos.
    - **Acidental:** Erros humanos sem má intenção.
    - **Estrutural:** Falhas de hardware ou software.
    - **Ambiental:** Desastres naturais ou causados pelo homem.
- A **Análise Quantitativa** atribue um valor monetário ao risco.
    - **Cálculos Chave:**
        - O cálculo principal que estima o custo anual de um risco é conhecido como **ALE (Expectativa de Perda Anual)**. Ele ajuda a decidir se o custo de uma contramedida vale a pena.
- Já a **Análise Qualitativa** prioriza riscos usando escalas descritivas (baixo, médio, alto).
    - **Ferramenta:** Utiliza uma *Matriz de Risco* (ou Mapa de Calor), que cruza a probabilidade de um evento com o impacto que ele causaria.

---

#### Controles de Segurança

- São as proteções ou contramedidas que implementamos para mitigar os riscos.
- **Classificação por Categoria:**
    - **Técnicos (ou Lógicos):** Implementados via tecnologia (ex: firewalls, criptografia, antivírus).
    - **Administrativos:** Políticas, procedimentos e padrões definidos pela gerência (ex: política de senhas, treinamento de conscientização).
    - **Físicos:** Protegem o acesso físico aos equipamentos (ex: trancas, câmeras de segurança, guardas).
- **Classificação por Função:**
    - **Preventivos:** Tentam **impedir** que um incidente aconteça (ex: firewall, senhas fortes).
    - **Dissuasivos:** Tentam **desencorajar** um atacante (ex: avisos de "você está sendo monitorado").
    - **De Detecção: Identificam** um incidente que está acontecendo ou já aconteceu (ex: sstema de detecção de intrusão, logs de auditoria).
    - **Corretivos: Corrigem** um sistema após um incidente (ex: restaurar um arquivo de um backup).
    - **De Recuperação: Restauram** a funcionalidade do negócio após um desastre (ex: ativar um servidor de backup em outro local).
    - **Compensatórios:** Fornecem uma alternativa quando um controle principal não pode ser implementado (ex: usar monitoramento extra se a criptografia não for viável).

---