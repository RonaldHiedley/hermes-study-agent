# Teste: analytics difficulties

## Objetivo

Verificar se o Hermes identifica corretamente dificuldades recorrentes.

## Pré-condição

Existem 2 sessões diferentes com:

- tópico: função composta;
- dificuldade: domínio.

Sessão 1:
- dificuldade: domínio

Sessão 2:
- dificuldade: domínio

## Entrada

Analytics difficulties

## Resultado esperado

O Hermes deve informar:

[DADOS REGISTRADOS]

- domínio apareceu na Sessão 1;
- domínio apareceu na Sessão 2.

[ANÁLISE]

- domínio apareceu em 2 sessões diferentes;
- portanto, é uma dificuldade recorrente segundo a regra da skill.

[SUGESTÕES]

- qualquer sugestão deve ser claramente identificada como sugestão;
- não deve ser apresentada como conclusão dos dados.

## Não deve

- afirmar que domínio é a "maior" dificuldade;
- afirmar causalidade;
- criar uma prioridade numérica;
- modificar sessões.
