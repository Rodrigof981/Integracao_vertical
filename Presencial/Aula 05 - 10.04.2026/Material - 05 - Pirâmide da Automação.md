# 📘 Aula 05 — Pirâmide da Automação na Integração Vertical

---

## 🏗️ 1. Pirâmide da Automação

A **Pirâmide da Automação** representa a organização dos sistemas industriais em níveis hierárquicos.

Cada nível possui uma função específica, e todos trabalham de forma integrada.

👉 A lógica é simples:
- níveis baixos → executam o processo  
- níveis intermediários → controlam e monitoram  
- níveis altos → planejam e decidem  

---

## 🔻 2. Nível 1 — Sensores e Atuadores (Chão de fábrica)

Este é o nível mais básico da pirâmide.

### 🔍 Função
- Coletar dados do processo (sensores)
- Executar ações físicas (atuadores)

---

### 📡 Sensores (entrada de dados)

Medem variáveis como:
- temperatura
- pressão
- nível
- velocidade
- proximidade

---

### ⚙️ Atuadores (ação)

Executam comandos:
- motores
- válvulas
- esteiras
- cilindros pneumáticos

---

### 💡 Exemplos práticos

#### 🏭 Linha de produção
- Sensor detecta presença de peça
- Atuador ativa braço robótico

---

#### 🌡️ Controle de temperatura
- Sensor mede 85°C
- Atuador liga sistema de resfriamento

---

#### 🚗 Indústria automotiva
- Sensor identifica posição do carro
- Atuador movimenta braço de solda

---

👉 Esse nível **não toma decisões complexas**, apenas mede e executa.

---

## 🔻 3. Nível 2 — Controle (CLP / SDCD)

Responsável por tomar decisões automáticas com base nos dados recebidos.

---

### 🧠 Função
- Receber dados dos sensores
- Processar lógica de controle
- Enviar comandos aos atuadores

---

### ⚙️ Principais dispositivos
- CLP (Controlador Lógico Programável)
- SDCD (Sistema Distribuído)
- CNC (máquinas industriais)

---

### 💡 Exemplos práticos

#### 🏭 Controle de esteira
- Sensor detecta peça
- CLP liga motor da esteira

---

#### 🌡️ Controle automático
- Regra: se temperatura > 80°C → ligar ventilador
- CLP executa automaticamente

---

#### 🧃 Fábrica de bebidas
- Sensor detecta garrafa cheia
- CLP envia comando para fechar tampa

---

#### ⚡ Sistema elétrico
- Sensor detecta sobrecarga
- CLP desliga circuito para segurança

---

👉 Esse nível executa decisões **rápidas e automáticas (milissegundos)**.

---

## 🔻 4. Nível 3 — Supervisão (SCADA / IHM)

Responsável por **visualizar e monitorar o processo**.

---

### 🖥️ Função
- Exibir dados em tempo real
- Permitir interação do operador
- Registrar histórico

---

### 🧰 Ferramentas
- SCADA (sistema supervisório)
- IHM (interface homem-máquina)

---

### 💡 Exemplos práticos

#### 🏭 Painel de controle
- Operador vê:
  - produção atual
  - temperatura
  - status das máquinas

---

#### 🚨 Alarmes
- Sistema mostra alerta:
  - "Máquina parada"
  - "Temperatura alta"

---

#### 📊 Histórico
- SCADA registra:
  - produção por hora
  - falhas ocorridas
  - tempo de parada

---

#### 🎛️ Controle manual
- Operador pode:
  - ligar/desligar máquina
  - ajustar velocidade

---

👉 Esse nível permite **interação humana com o sistema**.

---

## 🔻 5. Nível 4 — MES (Execução da Produção)

Responsável por gerenciar a produção em tempo real.

---

### ⚙️ Função
- Controlar ordens de produção (OP)
- Gerenciar recursos
- Monitorar desempenho
- Ajustar produção conforme necessidade

---

### 💡 Exemplos práticos

#### 🏭 Ordem de produção
- Produzir 1000 peças
- MES define:
  - qual máquina usar
  - em qual ordem produzir

---

#### 🔄 Reação a problemas
- Máquina quebra
- MES redireciona produção para outra máquina

---

#### 👷 Gestão de operadores
- MES identifica:
  - qual operador está na máquina
  - produtividade por turno

---

#### 📈 Eficiência (OEE)
- Máquina disponível: 8h  
- Produziu só 5h  
- MES calcula eficiência

---

#### 🧾 Rastreabilidade
- Produto rastreado:
  - lote
  - máquina
  - operador
  - horário

---

👉 Esse nível garante que o planejamento **aconteça de verdade**.

---

## 🔻 6. Nível 5 — ERP (Gestão)

Topo da pirâmide — responsável pela gestão da empresa.

---

### 🧠 Função
- Planejar produção
- Gerenciar recursos
- Controlar financeiro
- Integrar setores da empresa

---

### 💡 Exemplos práticos

#### 📦 Pedido de cliente
- Cliente pede 5000 peças
- ERP:
  - gera ordem de produção
  - calcula custo
  - verifica estoque

---

#### 🛒 Compras automáticas
- Estoque baixo
- ERP gera pedido ao fornecedor

---

#### 💰 Controle financeiro
- Venda realizada
- Sistema atualiza caixa automaticamente

---

#### 📊 Decisão estratégica
- ERP identifica:
  - produto mais vendido
  - produto com maior lucro
- Empresa ajusta produção

---

#### 🏭 Planejamento de produção
- ERP decide aumentar produção em 20%
- MES executa essa decisão

---

👉 Esse nível trabalha com **decisões estratégicas e planejamento**.

---

## 🔄 7. Integração entre os níveis (exemplo completo)

### 🧃 Exemplo: Fábrica de refrigerante

1. **ERP**
   - recebe pedido de 10.000 garrafas  

2. **MES**
   - organiza produção  
   - define máquinas  

3. **SCADA**
   - mostra processo em tempo real  

4. **CLP**
   - controla enchimento e tampagem  

5. **Sensores**
   - detectam nível da garrafa  

6. **Atuadores**
   - param enchimento quando atinge limite  

---

### 🔁 Situação de problema

- Sensor detecta erro (garrafa mal posicionada)
- CLP para máquina
- SCADA mostra alarme
- MES registra falha
- ERP recebe impacto na produção

---

👉 Todos os níveis trabalham juntos.

---

## 📈 8. Principais aprendizados

- Cada nível da pirâmide tem uma função específica  
- Os níveis mais baixos executam  
- Os níveis intermediários controlam  
- Os níveis superiores decidem  
- A integração entre níveis permite:
  - automação eficiente
  - decisões rápidas
  - controle total da produção  

---

## 🎯 9. Conclusão

A Pirâmide da Automação mostra como uma indústria funciona de forma organizada e integrada.

👉 Sem essa estrutura:
- sistemas ficam isolados  
- produção perde eficiência  

👉 Com essa estrutura:
- a indústria funciona como um sistema único, conectado e inteligente  

---