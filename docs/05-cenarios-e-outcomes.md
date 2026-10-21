# 05. Cenarios e Outcomes

## Matriz de cenarios

| Cenario | Objetivo | Perfil de risco | Resultado observado |
|---|---|---|---|
| S1 | Validar patch-fix para vulnerabilidade introduzida | Alto risco introduzido no PR | Reprovado |
| S2 | Validar bloqueio para vulnerabilidade critica | Risco critico introduzido | Reprovado |
| S3 | Validar major upgrade com incerteza de compatibilidade | Alto risco com potencial impacto funcional | Reprovado |
| S4 | Validar vulnerabilidade pre-existente fora do diff | Risco pre-existente | Aprovado |
| S5 | Validar fluxo sem findings | Sem risco relevante | Aprovado |

## Leitura tecnica do resultado

- S1-S3 reprovados mostram postura conservadora do gate para riscos introduzidos.
- S4 aprovado demonstra tolerancia controlada para risco historico, conforme politica escolhida.
- S5 aprovado confirma baseline limpa e funcionamento esperado da cadeia.

## Evidencia operacional

Cada execucao deve ser explicada pelo sumario do gate consolidado, que lista os motivos objetivos de aprovacao ou reprova.
