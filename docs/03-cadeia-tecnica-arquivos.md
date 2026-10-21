# 03. Cadeia Tecnica de Arquivos

## Camada 1 - Workflow de entrada

Arquivo principal do projeto aplicacao:

- dispara em Pull Request para branch alvo;
- recebe input opcional de cenario para simulacao deterministica;
- chama workflow de orquestracao reutilizavel.

## Camada 2 - Workflow de orquestracao

Workflow reutilizavel que:

- define parametros comuns (runner, severidade, cobertura);
- executa jobs de qualidade e seguranca;
- coleta resultados e aciona gate consolidado.

## Camada 3 - Jobs reutilizaveis

Conjunto de jobs independentes:

- build/test/coverage;
- SAST (CodeQL);
- dependency review;
- SCA custom de lockfile;
- gate de consolidacao;
- cd-ready.

## Camada 4 - Action custom e script

Action de SCA encapsula o script de avaliacao:

- consulta advisories por API;
- usa fallback para auditoria local de dependencias;
- aplica politica por severidade e origem do risco;
- retorna contrato de saida padrao para o gate.

## Contrato entre componentes

Padrao de interoperabilidade:

- valid: True/False
- validation_response: JSON com bool e log explicativo

Esse contrato reduz acoplamento e facilita substituicao de componentes.
