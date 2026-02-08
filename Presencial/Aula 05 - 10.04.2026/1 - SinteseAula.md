# Síntese da Aula 05

**Disciplina:** Integração Vertical e Horizontal  
**Docente:** Prof. Me. Deivison S. Takatu  
**Data:** 10/04/2026  
**Tema:** Pirâmide da Automação

---

## Pontos centrais discutidos

A quinta aula apresentou a Pirâmide da Automação como modelo conceitual para representar a hierarquia dos sistemas em um ambiente industrial integrado. O professor detalhou cada nível da pirâmide e explicou como a comunicação entre eles viabiliza a integração vertical.

## Estrutura da Pirâmide da Automação

A pirâmide organiza os sistemas industriais em cinco níveis funcionais, do mais próximo ao processo físico ao mais voltado à estratégia organizacional:

| Nível | Denominação | Função principal |
|-------|-------------|-----------------|
| 1 | Dispositivos de campo | Sensores e atuadores que interagem diretamente com o processo: coletam grandezas físicas e executam comandos. |
| 2 | Controle | CLPs e SDCDs que processam sinais em tempo real, executam lógica de controle e tomam decisões automáticas conforme parâmetros programados. |
| 3 | Supervisão | Sistemas SCADA e IHMs que apresentam o estado do processo ao operador, registram dados históricos e permitem intervenção manual quando necessário. |
| 4 | Gerenciamento de produção | Sistemas MES que coordenam a execução fabril: sequenciamento, alocação de recursos, controle de qualidade e cálculo de indicadores como OEE. |
| 5 | Gestão corporativa | Sistemas ERP que integram planejamento financeiro, compras, vendas, logística e recursos humanos, fornecendo visão estratégica consolidada. |

## Relação com a integração vertical

A pirâmide constitui a representação gráfica do conceito de integração vertical: os dados nascem no nível 1 (campo) e fluem progressivamente até o nível 5 (gestão), sendo tratados, filtrados e consolidados em cada camada intermediária. Sem essa estrutura hierárquica de comunicação, os sistemas operam como ilhas isoladas, e a gestão não dispõe de informações confiáveis sobre a realidade operacional.

## Observações

O conteúdo desta aula fornece fundamentação direta para o Projeto Integrador III, cuja arquitetura replica — em escala didática — os níveis da pirâmide: sensores (nível 1), ESP32 (nível 2), supervisório/dashboard (nível 3), e integração com camada de gestão via dashboard gerencial (níveis 4-5).
