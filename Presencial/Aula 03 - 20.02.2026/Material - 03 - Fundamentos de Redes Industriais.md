# Aula 03 — Fundamentos de Redes Industriais  

---

## 🧭 Capítulo 1 — Por que Redes Industriais Existem?

## 1.1 Perguntas Norteadoras

Inicie a aula provocando os estudantes:

- Como um **sensor** “fala” com um CLP?  
- Como um **CLP envia dados para um supervisório?**  
- Como os dados chegam ao **ERP da empresa?**

Essas perguntas evidenciam que a automação moderna depende de **comunicação estruturada e confiável**.

---

## 1.2 Comunicação na Automação

A automação industrial não é apenas controle de máquinas — é **troca contínua de informações**.

As redes industriais existem para:

- conectar sensores, atuadores e controladores;
- permitir monitoramento em tempo real;
- garantir sincronização entre dispositivos;
- viabilizar integração vertical com sistemas MES e ERP.

Sem rede → não há fluxo de dados → não há integração vertical.

---

# 🖧 Capítulo 2 — Rede Industrial × Rede Corporativa (TI)

## 2.1 Diferenças Fundamentais

| Rede Industrial | Rede Corporativa |
|-----------------|-----------------|
| Comunicação em tempo real | Comunicação não determinística |
| Alta confiabilidade | Foco em dados administrativos |
| Ambiente hostil | Ambiente controlado |
| Determinismo | Melhor esforço (best effort) |

---

## 2.2 Pontos de Destaque

### ⏱️ Tempo de Resposta
Na indústria, milissegundos podem impactar:
- sincronismo de motores;
- precisão de processos;
- segurança operacional.

### 🛡️ Robustez
Ambientes industriais possuem:
- ruído elétrico;
- vibração;
- altas temperaturas;
- poeira e umidade.

Equipamentos de rede precisam ser projetados para esse contexto.

### ⚡ Interferência Elétrica
Diferente de escritórios, o chão de fábrica possui:
- inversores de frequência;
- motores;
- cargas indutivas.

Isso exige cabeamento adequado e proteção contra ruídos.

### 🔄 Disponibilidade
Parada de rede industrial pode significar:
- parada de produção;
- prejuízo financeiro;
- risco operacional.

---

# 🔌 Capítulo 3 — Elementos de uma Rede Industrial

## 3.1 Dispositivos de Campo

### Sensores
Responsáveis por coletar dados físicos:
- temperatura
- pressão
- nível
- proximidade

### Atuadores
Executam ações físicas:
- válvulas
- motores
- cilindros pneumáticos

---

## 3.2 Controle

### CLPs (Controladores Lógicos Programáveis)
- Processam sinais de entrada;
- Executam lógica de controle;
- Enviam comandos aos atuadores.

---

## 3.3 Supervisão

### IHMs
Interface homem-máquina para operação local.

### Sistemas Supervisórios (SCADA)
Permitem:
- monitoramento remoto;
- registro histórico;
- análise de desempenho.

---

## 3.4 Infraestrutura de Comunicação

### Switch Industrial
- Interliga dispositivos na rede;
- Projetado para ambiente hostil;
- Alta confiabilidade.

### Gateway
- Converte protocolos;
- Integra redes diferentes;
- Permite comunicação com sistemas de TI.

---

# 🎯 Capítulo 4 — Síntese da Aula

Ao final da aula, o estudante deve compreender que:

- Redes industriais são a base da integração de sistemas.
- Elas diferem significativamente das redes de TI.
- Precisam ser determinísticas, robustas e confiáveis.
- Conectam dispositivos do nível de campo ao nível supervisório.
- São fundamentais para viabilizar integração vertical.

