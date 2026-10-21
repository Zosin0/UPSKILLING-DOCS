# 01. Visao Geral

## Contexto

A iniciativa aplica DevSecOps Shift Left para antecipar validacoes de qualidade e seguranca no momento do Pull Request, reduzindo retrabalho em fases tardias e aumentando previsibilidade de entrega.

## Problema que estava sendo atacado

- verificacoes fragmentadas entre times e ferramentas;
- pouca padronizacao de criterio de aprovacao;
- dificuldade de explicar tecnicamente por que um PR foi aprovado ou bloqueado.

## Solucao proposta

Uma cadeia de GitHub Actions reutilizavel com:

- workflow de entrada no repositorio da aplicacao;
- workflow de orquestracao reutilizavel;
- jobs reutilizaveis de qualidade e seguranca;
- gate consolidado para decisao unica;
- etapa final de prontidao para deploy.

## Resultado esperado

- visibilidade clara do estado de risco por PR;
- decisao auditavel de pass/fail;
- base de reuso para multiplos projetos.
