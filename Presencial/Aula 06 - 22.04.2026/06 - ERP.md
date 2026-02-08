# 📘 Aula 06 — Sistemas ERP na Integração Industrial  

---

## 🧭 Capítulo 1 — Contextualização do ERP

### 1.1 O ERP dentro da Integração de Sistemas

Na evolução da disciplina, já compreendemos:

- Redes industriais → comunicação  
- SDCD/CLP → controle  
- SCADA → supervisão  
- MES → execução  

Agora chegamos ao **nível mais alto da pirâmide**: o **ERP (Enterprise Resource Planning)**.

👉 O ERP é responsável por **integrar e gerenciar toda a empresa**, conectando:

- Produção  
- Logística  
- Financeiro  
- Compras  
- Vendas  
- Recursos humanos  
- Entre outros setores

Ele transforma dados operacionais em **decisões estratégicas**.

---

### 1.2 Papel do ERP na Indústria

O ERP não atua diretamente no chão de fábrica.

Ele atua no nível **estratégico e gerencial**, sendo responsável por:

- Planejar a produção  
- Controlar recursos  
- Integrar setores  
- Apoiar a tomada de decisão  

👉 Ele responde perguntas como:

- O que produzir?  
- Quando produzir?  
- Quanto produzir?  
- Quanto isso vai custar?  

---

## 🏗️ Capítulo 2 — Conceito de ERP

### 2.1 Definição

O **ERP (Enterprise Resource Planning)** é um sistema integrado de gestão que centraliza informações e processos de toda a organização em uma única plataforma.

---

### 2.2 Características principais

Um ERP possui:

- Base de dados única  
- Módulos integrados  
- Atualização em tempo real  
- Padronização de processos  

👉 Isso evita:

- Retrabalho  
- Inconsistência de dados  
- Falhas de comunicação  

---

### 2.3 ERP como sistema integrador

Sem ERP:
- Setores isolados  
- Planilhas desconectadas  
- Decisões imprecisas  

Com ERP:
- Visão global da empresa  
- Dados consistentes  
- Decisões mais rápidas  

---

## 🧩 Capítulo 3 — Módulos de um ERP

### 3.1 Principais módulos

#### 💰 Financeiro
- Contas a pagar/receber  
- Fluxo de caixa  
- Faturamento  

---

#### 🛒 Compras
- Gestão de fornecedores  
- Pedidos de compra  
- Controle de suprimentos  

---

#### 📦 Estoque
- Controle de materiais  
- Entrada e saída  
- Inventário  

---

#### 🏭 Produção (PCP)
- Planejamento da produção  
- Ordens de produção  
- Controle de capacidade  

---

#### 📈 Vendas
- Pedidos de clientes  
- Faturamento  
- Histórico de vendas  

---

#### 👥 Recursos Humanos
- Folha de pagamento  
- Gestão de colaboradores  
- Avaliação de desempenho  

---

### 3.2 Integração entre módulos

A principal força de um ERP está na **integração automática entre os módulos**, permitindo que uma ação em um setor gere impactos imediatos em toda a empresa.

👉 Isso elimina retrabalho, reduz erros e garante consistência dos dados.

---

### 🔄 Exemplos de Integração

- Venda realizada → atualiza financeiro, estoque e faturamento  
- Produção iniciada → consome matéria-prima do estoque  
- Estoque baixo → gera solicitação de compra  
- Compra realizada → atualiza contas a pagar  
- Produto entregue → gera faturamento automático  
- Funcionário alocado → impacta custo de produção  
- Ordem de produção finalizada → atualiza estoque de produto acabado  
- Atraso na produção → impacta prazo de entrega ao cliente  

---

### 📊 Tabela de Integração entre Módulos

| Evento | Módulo de Origem | Módulos Impactados | Resultado |
|-------|-----------------|-------------------|----------|
| Venda realizada | Vendas | Financeiro, Estoque | Geração de receita e baixa no estoque |
| Emissão de nota fiscal | Vendas | Financeiro | Registro de contas a receber |
| Produção iniciada | Produção (PCP) | Estoque | Consumo de matéria-prima |
| Produção finalizada | Produção | Estoque, Vendas | Entrada de produto acabado disponível |
| Estoque mínimo atingido | Estoque | Compras | Geração automática de pedido de compra |
| Pedido de compra aprovado | Compras | Financeiro | Geração de contas a pagar |
| Recebimento de material | Compras | Estoque | Atualização do inventário |
| Pagamento a fornecedor | Financeiro | Compras | Baixa de obrigação financeira |
| Contratação de funcionário | RH | Financeiro | Impacto na folha de pagamento |
| Alocação de operador na produção | RH | Produção | Atualização de custo operacional |
| Atraso na produção | Produção | Vendas, Logística | Reprogramação de entrega |
| Devolução de produto | Vendas | Estoque, Financeiro | Ajuste de estoque e estorno financeiro |

---

### 💡 Interpretação

👉 Perceba que:

- Nenhum módulo funciona isoladamente  
- Um único evento pode impactar vários setores  
- A informação flui automaticamente pela empresa  

---

### 🚀 Conclusão da Integração

A integração entre módulos transforma o ERP em um **sistema nervoso da organização**, onde:

- informações circulam em tempo real  
- decisões são baseadas em dados confiáveis  
- processos acontecem de forma sincronizada  

👉 Isso é o que permite uma gestão moderna, eficiente e orientada a dados.

---

## 🏭 Capítulo 4 — Exemplo Prático

### 🧃 Fábrica de bebidas

#### 1. Pedido
Cliente solicita 10.000 unidades  

ERP:
- Registra venda  
- Calcula custo  
- Verifica estoque  

---

#### 2. Planejamento
ERP:
- Gera ordem de produção  
- Envia ao MES  

---

#### 3. Execução
MES:
- Distribui produção  
- Planeja a utilização das máquinas

---

#### 4. Produção
CLP + sensores:
- Executam processo  

---

#### 5. Monitoramento
SCADA:
- Exibe dados em tempo real  

---

#### 6. Retorno
ERP recebe:
- Produção realizada  
- Custos  
- Tempo  
- Outros Indicadores

---

## ✅ Conclusão

O ERP consolida a integração da empresa ao transformar dados operacionais em **informação gerencial útil**.

Seu principal valor não está apenas no controle, mas na capacidade de:

- alinhar planejamento e execução  
- dar visibilidade do negócio como um todo  
- permitir respostas rápidas a mudanças  

👉 Na prática, ele garante que o que foi planejado realmente aconteça — e que possa ser ajustado com base em dados reais.

Assim, o ERP fecha o ciclo da integração vertical, conectando operação e estratégia de forma contínua.

---