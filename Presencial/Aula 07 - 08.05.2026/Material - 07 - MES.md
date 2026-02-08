# 📘 Aula 07 — Sistemas MES na Integração Industrial

---

# 🧭 1. Visão Geral

Em uma indústria, diferentes sistemas trabalham juntos:

- **Sensores e atuadores** → medem e executam ações físicas  
- **CLP (Controlador Lógico Programável)** → controla máquinas automaticamente  
- **SCADA (Supervisory Control and Data Acquisition)** → supervisão e monitoramento em telas  
- **ERP (Enterprise Resource Planning)** → gestão empresarial e planejamento  
- **MES (Manufacturing Execution System)** → execução da produção em tempo real  

👉 O MES fica entre o ERP e a automação, conectando gestão e fábrica.

---

# 🏗️ 2. O que é MES?

O **MES (Sistema de Execução da Manufatura)** é o software responsável por acompanhar, controlar e registrar a produção enquanto ela acontece.

Ele transforma ordens planejadas no ERP em atividades reais no chão de fábrica.

### O MES responde:

- O que está sendo produzido?  
- Em qual máquina?  
- Qual operador está trabalhando?  
- Quantas peças foram feitas?  
- Houve parada ou falha?  
- A meta está sendo atingida?  

---

# 🔄 3. Fluxograma do MES na Indústria

    +----------------------+
    | ERP                  |
    | Planejamento Geral   |
    | Pedidos / Estoque    |
    +----------+-----------+
               |
               v
    +----------------------+
    | MES                  |
    | Execução da Produção |
    | Ordens / Qualidade   |
    | Indicadores / OEE    |
    +----+------------+----+
         |            |
         v            v
+----------------+   +----------------+
| SCADA          |   | Banco de Dados |
| Supervisão     |   | Histórico      |
+-------+--------+   +----------------+
        |
        v
+----------------------+
| CLP + Sensores       |
| Máquinas / Processo  |
+----------------------+

👉 O ERP planeja, o MES coordena, o SCADA monitora e o CLP executa.

---

# 🧩 4. Principais Funções do MES

## 📦 Ordens de Produção

- liberar ordens  
- iniciar e finalizar produção  
- acompanhar metas  

## 🏭 Recursos

- máquinas disponíveis  
- operadores habilitados  
- materiais necessários  

## 📡 Coleta de Dados

Recebe dados de sensores, máquinas e operadores.

## ✅ Qualidade

- inspeções  
- defeitos  
- refugos  
- aprovação de lotes  

## 🔎 Rastreabilidade

Mostra:

- lote usado  
- máquina utilizada  
- horário  
- operador responsável  

## 📊 Indicadores

Calcula automaticamente:

- produtividade  
- tempo parado  
- taxa de defeitos  
- **OEE (Overall Equipment Effectiveness)** = eficiência global da máquina  

---

# 🏭 5. Exemplo Prático

## Fábrica de Bebidas

1. ERP recebe pedido de 10.000 garrafas  
2. MES define linha e turno  
3. CLP controla enchimento  
4. SCADA mostra produção em tempo real  
5. MES registra perdas e desempenho  
6. ERP recebe resultado final  

---

# 🔌 6. Integrações Importantes

## ERP ↔ MES

Troca:

- ordens de produção  
- consumo de materiais  
- quantidades produzidas  
- custos reais  

## MES ↔ SCADA / CLP

Troca:

- status da máquina  
- alarmes  
- contadores  
- parâmetros de processo  

## MES ↔ BI

**BI (Business Intelligence)** = painéis e relatórios para análise gerencial.

---

# ⚖️ 7. Benefícios

- produção visível em tempo real  
- menos desperdício  
- decisões mais rápidas  
- dados confiáveis  
- melhor produtividade  
- base para Indústria 4.0  

---

# ⚠️ 8. Desafios

- integrar sistemas antigos  
- treinar equipes  
- padronizar dados  
- investir em rede e infraestrutura  

---

# 🎯 9. Conclusão

O **MES** é a ponte entre o planejamento do ERP e a execução das máquinas.

Sem ele, a empresa planeja e produz de forma desconectada.  
Com ele, a fábrica se torna integrada, rastreável e orientada por dados.

---

## 📚 Referências Bibliográficas (ABNT NBR 6023:2018)

SAENZ DE UGARTE, B.; ARTIBA, A.; PELLERIN, R. Manufacturing execution system – a literature review. *Production Planning & Control*, v. 20, n. 6, p. 525–539, 2009. DOI: 10.1080/09537280902938613.

ARICA, E.; POWELL, D. J. Status and future of manufacturing execution systems. In: *Proceedings of the 2017 IEEE International Conference on Industrial Engineering and Engineering Management (IEEM)*. [S.l.]: IEEE, 2017. p. 2000–2004.