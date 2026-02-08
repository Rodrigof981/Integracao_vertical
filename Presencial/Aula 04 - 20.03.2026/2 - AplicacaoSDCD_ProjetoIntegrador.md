# Análise — Aplicação de SDCD no Projeto Integrador

## Enunciado

Com base nos conceitos estudados sobre Sistemas Digitais de Controle Distribuído (SDCD), realizar uma análise de como um sistema desse tipo poderia ser aplicado no Projeto Integrador, considerando a seguinte arquitetura: Sensor de Temperatura → ESP32 → MQTT → Servidor → Aplicativo Mobile → Dashboard → Gestão da Fábrica.

---

## Desenvolvimento

### Correspondência entre a arquitetura proposta e os princípios do SDCD

A arquitetura definida para o Projeto Integrador III (PII3) materializa, em escala reduzida, a lógica operacional dos sistemas de controle distribuído empregados em plantas industriais de grande porte. O conceito central permanece o mesmo: descentralizar o processamento, posicionando inteligência computacional junto ao ponto de medição e transmitindo informações processadas para camadas superiores de supervisão e decisão. Conforme Lara (2021), essa abordagem constitui a base das arquiteturas modernas de automação, nas quais a proximidade entre o controlador e o processo monitorado assegura tempos de resposta compatíveis com as exigências operacionais.

### Função de cada componente

O **sensor de temperatura** representa o elemento primário de aquisição. Sem ele, o sistema opera às cegas. Sua função é converter fenômenos térmicos em sinais elétricos mensuráveis, posicionando-se diretamente no ambiente produtivo.

O **ESP32** atua como controlador local distribuído. Diferentemente de um sistema centralizado que exigiria condução de todos os sinais até um ponto único, o ESP32 processa localmente o dado adquirido, aplica filtragens e o encapsula para transmissão. Essa autonomia local é a essência do paradigma distribuído descrito por Groover (2011): a capacidade de cada nó executar lógica de controle independente da disponibilidade imediata da rede.

O **protocolo MQTT**, baseado no modelo publicação/assinatura, viabiliza a comunicação assíncrona entre o dispositivo de campo e o servidor. Conforme a especificação mantida pela OASIS (2019), o protocolo foi projetado para ambientes com largura de banda restrita e conexões instáveis, tornando-o adequado a cenários industriais com dispositivos de recursos limitados.

O **servidor** consolida as mensagens recebidas, persiste dados em banco, aplica validações e disponibiliza informações via interface programática. Corresponde funcionalmente à estação de supervisão dos sistemas SDCD tradicionais.

O **aplicativo mobile** e o **dashboard** constituem interfaces de acesso à informação processada. O primeiro amplia a mobilidade do gestor; o segundo oferece representação gráfica consolidada do estado operacional — equivalente funcional de um sistema SCADA simplificado.

### Fluxo de dados

O ciclo tem início no fenômeno físico: o sensor registra a temperatura do ambiente ou equipamento monitorado. O ESP32 executa leituras periódicas, converte o sinal analógico em valor numérico e publica o dado em tópico MQTT pré-definido. O broker MQTT roteia a mensagem ao servidor inscrito naquele tópico. O servidor persiste o registro, verifica se o valor extrapola limiares configurados e atualiza a API de consulta. As interfaces consomem essa API e apresentam gráficos de tendência, valores instantâneos e alertas visuais quando condições anômalas são detectadas.

### Decisões viabilizadas pelo sistema

A informação consolidada no dashboard habilita ações concretas:

- Identificação de sobreaquecimento em estágio inicial, permitindo intervenção preventiva antes de dano ao equipamento.
- Correlação entre variações térmicas e parâmetros de produção para ajuste de receitas de processo.
- Geração de histórico rastreável para auditorias de qualidade e conformidade com normas ambientais.
- Suporte a estratégias de manutenção baseada em condição, substituindo manutenção puramente corretiva.

### Vantagens da abordagem distribuída neste contexto

A distribuição do controle proporciona benefícios estruturais ao projeto:

- **Resiliência a falhas isoladas:** a indisponibilidade de um ESP32 afeta exclusivamente seu ponto de medição, preservando o restante da rede operacional.
- **Economia em infraestrutura física:** a comunicação sem fio entre ESP32 e broker elimina cabeamento extenso entre campo e sala de controle.
- **Expansibilidade incremental:** novos pontos de monitoramento são integrados pela simples adição de dispositivos e tópicos MQTT, sem alteração da arquitetura existente.
- **Autonomia local:** o ESP32 pode executar lógicas de alerta ou atuação emergencial mesmo durante perda temporária de conectividade com o servidor.
- **Visão integrada sem fragmentação:** o dashboard consolida dados de múltiplos nós distribuídos em visualização única, replicando o princípio do SDCD de supervisão centralizada com controle descentralizado.

---

## Referências

GROOVER, M. P. *Automação industrial e sistemas de manufatura*. São Paulo: Pearson, 2011.

LARA, Carla Eduarda Orlando de Moraes de. *Automação e controle industrial*. Curitiba: Contentus, 2021.

OASIS. MQTT Version 5.0: OASIS Standard. Burlington: OASIS Open, 2019. Disponível em: https://docs.oasis-open.org/mqtt/mqtt/v5.0/mqtt-v5.0.html. Acesso em: 20 mar. 2026.
