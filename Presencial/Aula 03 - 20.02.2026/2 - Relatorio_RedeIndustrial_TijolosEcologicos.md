# Relatório Técnico — Implantação de Rede Industrial em Fábrica de Tijolos Ecológicos

## Introdução

Este relatório apresenta a proposta de implantação de uma infraestrutura de rede industrial para uma unidade fabril de médio porte, localizada na região de Sorocaba (SP), dedicada à produção de tijolos ecológicos. Diferentemente do tijolo cerâmico convencional, cuja fabricação depende de fornos a lenha ou gás, o tijolo ecológico é produzido pelo processo de prensagem hidráulica de uma composição de solo argiloso, cimento Portland e água, seguida de cura ao ar livre. Essa técnica elimina a etapa de queima e reduz significativamente a emissão de CO₂ no processo produtivo, conforme documentado pela Associação Brasileira de Cimento Portland (ABCP, 2020).

A escolha por rede industrial — em detrimento de soluções comerciais convencionais — justifica-se pelas condições ambientais da planta: presença constante de partículas de cimento em suspensão, vibrações geradas por prensas hidráulicas e necessidade de comunicação com baixa latência entre equipamentos de controle. Segundo Albuquerque e Alexandria (2009), redes industriais são projetadas exatamente para esses cenários, oferecendo determinismo, robustez e integração nativa com CLPs e supervisórios.

## Arquitetura proposta

A solução especifica o protocolo **EtherCAT** como backbone de comunicação, selecionado por sua capacidade de sincronismo em tempo real com ciclos de comunicação na ordem de microssegundos, adequação a topologias lineares típicas de linhas de produção sequenciais e simplicidade de cabeamento (BECKHOFF, 2023).

A arquitetura organiza-se em quatro níveis:

1. **Nível de campo:** sensores de umidade do solo, sensores de pressão nas prensas, encoders em esteiras transportadoras, atuadores pneumáticos para ejeção de peças.
2. **Nível de controle:** CLP Beckhoff CX5130 posicionado em painel central, com módulos de entrada/saída distribuídos ao longo da linha via terminais EtherCAT EK1100.
3. **Nível de supervisão:** estação de trabalho com software supervisório Ignition (Inductive Automation), conectada ao CLP via OPC UA para aquisição de dados e geração de históricos.
4. **Nível corporativo:** sistema ERP (Odoo) em servidor local, integrado ao supervisório por API REST para recebimento de dados de produção (quantidade de peças, tempo de ciclo, rejeitos).

```
Sensores/Atuadores
       │ (EtherCAT)
       ▼
Terminais I/O Distribuídos (EK1100)
       │ (EtherCAT)
       ▼
CLP Beckhoff CX5130
       │ (OPC UA)
       ▼
Supervisório Ignition
       │ (API REST)
       ▼
ERP Odoo (Gestão)
```

## Levantamento orçamentário

| Equipamento | Especificação | Fornecedor | Qtd. | Valor Unit. (R$) | Valor Total (R$) | Prazo |
|---|---|---|---|---|---|---|
| CLP compacto | Beckhoff CX5130, Intel Atom, EtherCAT Master | Beckhoff Brasil | 1 | 6.200,00 | 6.200,00 | 20 dias |
| Terminal EtherCAT | EK1100 Bus Coupler + módulos I/O (16 DI + 8 DO + 4 AI) | Beckhoff Brasil | 3 | 2.800,00 | 8.400,00 | 20 dias |
| Switch gerenciável | Hirschmann RS20, 8 portas, trilho DIN, IP20 | Westcon | 2 | 1.950,00 | 3.900,00 | 10 dias |
| Cabeamento | Cabo Cat5e industrial blindado SF/UTP, rolo 300 m | Lapp Group | 1 | 5.400,00 | 5.400,00 | 7 dias |
| Licença supervisório | Ignition Standard, tags ilimitados | Inductive Automation | 1 | 11.500,00 | 11.500,00 | Imediata |
| Sensores e atuadores | Kit: 6 sensores indutivos + 4 transdutores de pressão + 2 encoders + válvulas | Sense / SMC | 1 | 9.800,00 | 9.800,00 | 15 dias |
| **Total** | | | | | **45.200,00** | |

## Viabilidade e retorno

O investimento de R$ 45.200,00 posiciona-se abaixo de soluções baseadas integralmente em fabricantes tradicionais de automação. A adoção do EtherCAT permite expansão futura com custo marginal reduzido, visto que novos terminais I/O são adicionados em cascata sem necessidade de switches adicionais. Estima-se retorno entre 10 e 18 meses, considerando redução de refugo por controle automatizado de umidade e pressão, diminuição de paradas não programadas e maior rastreabilidade para certificação ambiental.

## Riscos identificados

- **Técnico:** incompatibilidade pontual de firmware entre módulos de diferentes lotes exige atenção na etapa de comissionamento.
- **Ambiental:** o nível de poeira de cimento demanda invólucros com grau de proteção IP54 ou superior para componentes expostos.
- **Dependência de fornecedor:** a padronização em Beckhoff exige estoque mínimo de peças de reposição e contrato de suporte técnico.
- **Cibersegurança:** a integração com o ERP via rede TCP/IP requer segmentação por VLAN e firewall entre o segmento industrial e o corporativo.

## Considerações finais

A implantação de rede industrial adequada ao ambiente fabril de tijolos ecológicos transforma dados de processo em informação gerencial estruturada, habilitando a organização a operar dentro dos princípios de integração vertical e digital. O investimento é compatível com operações de médio porte e oferece escalabilidade para futuras expansões de linha ou integração com plataformas de análise em nuvem.

---

## Referências

ABCP — Associação Brasileira de Cimento Portland. *Solo-cimento: solução para construção sustentável*. São Paulo: ABCP, 2020.

ALBUQUERQUE, Pedro U. B. de; ALEXANDRIA, Auzuir Ricardo de. *Redes industriais*. São Paulo: Ensino Profissional, 2009.

BECKHOFF. EtherCAT Technology Group — System Description. Beckhoff Automation, 2023. Disponível em: https://www.beckhoff.com/en-en/products/i-o/ethercat/. Acesso em: 20 fev. 2026.

GROOVER, M. P. *Automação industrial e sistemas de manufatura*. São Paulo: Pearson, 2011.
