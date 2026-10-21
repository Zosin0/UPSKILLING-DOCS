# 04. Ferramentas e Racional Tecnico

## Build/Test/Coverage

Por que usar:

- garantir baseline funcional antes de discutir remediacao;
- detectar quebra de comportamento imediatamente no PR;
- medir cobertura minima para reduzir risco de regressao silenciosa.

## SAST com CodeQL

Por que usar:

- identificar vulnerabilidades no codigo da aplicacao;
- complementar analise de dependencias;
- manter rastreabilidade de findings de seguranca de codigo.

## Dependency Review

Por que usar:

- controlar risco de supply chain no diff do PR;
- aplicar politica por severidade;
- prevenir entrada de dependencia insegura.

## SCA custom por lockfile

Por que usar:

- avaliar dependencias efetivamente resolvidas;
- considerar origem do risco (introduzido no PR ou pre-existente);
- permitir cenarios deterministicos para prova de conceito.

## Gate consolidado

Por que usar:

- gerar decisao unica de aprovacao/reprovacao;
- facilitar auditoria e governanca;
- tornar explicavel para time tecnico e banca.
