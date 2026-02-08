# Planejamento Estratégico — Integração Industrial: Suzano S.A. e JBS S.A.

## Enunciado

Considerando que ambas as empresas possuem processos industriais, elaborar um documento simulando um planejamento estratégico, contemplando a integração vertical entre os níveis hierárquicos da empresa (chão de fábrica, sistemas de controle e gestão) e a integração horizontal entre processos e áreas no mesmo nível, como produção, logística, fornecedores, clientes e diferentes unidades industriais, visando propostas da tecnologia da informação para aumentar integração ao longo da cadeia de valor.

---

## Desenvolvimento

### Contexto organizacional

A Suzano S.A. e a JBS S.A., embora pertençam a segmentos distintos, compartilham a característica de operar plantas industriais distribuídas geograficamente, com processos contínuos e semi-contínuos que demandam elevado nível de coordenação entre etapas operacionais. Ambas geram volumes expressivos de dados de processo, cuja integração adequada constitui fator determinante para a eficiência produtiva e a competitividade de mercado. O planejamento aqui proposto simula iniciativas de tecnologia da informação que ampliariam a articulação vertical e horizontal dessas organizações.

### Integração vertical — do equipamento ao planejamento

A integração vertical proposta estrutura-se em três camadas:

**Camada de campo e controle.** No nível operacional, sensores de processo (temperatura, pressão, umidade, peso, velocidade de esteira) alimentam CLPs responsáveis pelo controle em tempo real. Para a Suzano, isso se aplica ao monitoramento das caldeiras de recuperação, digestores de celulose e máquinas de papel. Na JBS, aplica-se às linhas de abate, câmaras de resfriamento e esteiras de embalagem. A padronização dos protocolos de comunicação — preferencialmente PROFINET ou OPC UA — é requisito para que esses dados alcancem camadas superiores de maneira estruturada (ALBUQUERQUE; ALEXANDRIA, 2009).

**Camada de supervisão e execução (MES/SCADA).** Sistemas supervisórios consolidam os dados de múltiplos CLPs, apresentam o estado operacional em tempo real e geram registros históricos. O MES traduz ordens de produção originadas no ERP em sequenciamento de máquinas, alocação de recursos e indicadores de desempenho. Segundo Saenz de Ugarte, Artiba e Pellerin (2009), essa camada intermediária é o que transforma dados brutos em informação gerencial acionável.

**Camada corporativa (ERP).** No nível superior, o sistema ERP consolida informações financeiras, de estoque, compras e vendas. A integração com o MES permite que o ERP receba dados reais de consumo, perdas e produtividade, substituindo estimativas por valores mensurados. Para a Suzano, essa conexão viabiliza ajustes dinâmicos no planejamento de colheita florestal conforme a demanda fabril. Na JBS, possibilita o balanceamento da capacidade de abate em diferentes plantas conforme pedidos consolidados do mercado externo.

### Integração horizontal — entre áreas, unidades e parceiros

No eixo horizontal, propõe-se:

- **Plataforma unificada de planejamento de vendas e operações (S&OP):** consolida previsões de demanda, capacidade produtiva e disponibilidade logística entre todas as unidades fabris. Na JBS, permite redistribuir volumes entre plantas conforme restrições sanitárias regionais. Na Suzano, permite equilibrar produção de celulose e papel conforme contratos de exportação e mercado interno.

- **Centro de dados corporativo:** todas as unidades industriais reportam indicadores padronizados a um repositório central, permitindo benchmarking interno, identificação de melhores práticas e detecção precoce de desvios. Dashboards gerenciais disponibilizam essa informação em tempo real para diretores de operações.

- **Integração com a cadeia externa via EDI e APIs:** conexão automatizada com fornecedores de insumos e transportadoras para sincronizar pedidos, entregas e estoques. Reduz lead times e permite resposta rápida a interrupções na cadeia de suprimentos.

### Tecnologias habilitadoras

A materialização dessas propostas depende de:

- Arquitetura de microsserviços e APIs REST para interoperabilidade entre sistemas legados e novas plataformas.
- Computação em nuvem híbrida para escalabilidade e acesso remoto às informações operacionais.
- Ferramentas de Business Intelligence integradas ao MES para análise de indicadores de OEE, refugo e consumo energético.
- Governança de dados formalizada com definição de proprietários, políticas de acesso e auditoria de integridade.

### Resultados esperados

A convergência entre integração vertical e horizontal, sustentada por tecnologia da informação, gera ganhos mensuráveis: redução de tempo de resposta a oscilações de demanda, diminuição de estoques intermediários, melhoria de indicadores de qualidade e fortalecimento da rastreabilidade ao longo de toda a cadeia de valor. Para organizações do porte da Suzano e JBS, esses ganhos se traduzem em milhões de reais preservados anualmente e em maior resiliência operacional frente a cenários adversos.

---

## Referências

ALBUQUERQUE, Pedro U. B. de; ALEXANDRIA, Auzuir Ricardo de. *Redes industriais*. São Paulo: Ensino Profissional, 2009.

CAIÇARA JÚNIOR, Cícero. *Sistemas integrados de gestão: ERP — uma abordagem gerencial*. Curitiba: Intersaberes, 2015.

SAENZ DE UGARTE, B.; ARTIBA, A.; PELLERIN, R. Manufacturing execution system – a literature review. *Production Planning & Control*, v. 20, n. 6, p. 525–539, 2009.

SUZANO S.A. Relatório Anual de Sustentabilidade 2023. São Paulo: Suzano, 2023. Disponível em: https://ri.suzano.com.br. Acesso em: 13 fev. 2026.

JBS S.A. Relatório Anual Integrado 2023. São Paulo: JBS, 2023. Disponível em: https://ri.jbs.com.br. Acesso em: 13 fev. 2026.
