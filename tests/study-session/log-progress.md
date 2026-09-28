# Teste: log-progress

## Objetivo

Verificar se o Hermes registra progresso incremental sem alterar dados não informados.

## Pré-condição

Existe uma sessão iniciada de matemática sobre funções.

## Entrada

Fiz 8 questões de função composta, acertei 6 e tive dificuldade em domínio.

## Resultado esperado

O Hermes deve:

- registrar 8 questões;
- registrar 6 acertos;
- calcular 75% de aproveitamento;
- adicionar "domínio" às dificuldades;
- manter `plannedDuration` inalterado;
- não inventar `actualDuration`;
- não finalizar a sessão automaticamente;
- pedir confirmação antes de salvar, conforme a skill.

## Não deve

- substituir a duração planejada pela duração real;
- criar uma nova sessão;
- inventar observações;
- alterar dados não informados.
