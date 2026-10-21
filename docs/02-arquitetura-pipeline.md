# 02. Arquitetura da Pipeline

## Fluxo macro

```mermaid
flowchart LR
  A[Workflow de Entrada] --> B[Workflow de Orquestracao]
  B --> C1[Build Test Coverage]
  B --> C2[SAST CodeQL]
  B --> C3[Dependency Review]
  B --> C4[SCA PR Head]
  C1 --> D[Gate Consolidado]
  C2 --> D
  C3 --> D
  C4 --> D
  D --> E[CD Ready]
```

## Principio de desenho

- controles executados como componentes reutilizaveis;
- outputs padronizados entre jobs;
- decisao final centralizada no gate;
- rastreabilidade por sumario de execucao.

## Beneficios arquiteturais

- padrao unico para equipes diferentes;
- manutencao simplificada por encapsulamento;
- escalabilidade com novos controles sem quebrar o fluxo base.
