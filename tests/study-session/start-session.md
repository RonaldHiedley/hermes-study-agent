# Teste: start-session

## Objetivo

Verificar se o Hermes inicia uma sessão corretamente.

## Entrada

Study: matemática, funções, 45 minutos, objetivo: entender função composta

## Resultado esperado

O Hermes deve:

- criar uma nova sessão;
- registrar automaticamente a data;
- registrar automaticamente o horário de início;
- registrar `subject: matemática`;
- registrar `topic: funções`;
- registrar `plannedDuration: 45 min`;
- registrar o objetivo;
- iniciar `questionsAttempted` em 0;
- iniciar `correct` em 0;
- iniciar `accuracy` em 0% ou equivalente;
- iniciar `difficulties` vazio;
- iniciar `observations` vazio;
- retornar um `session_id`;
- marcar a sessão como em andamento.

## Não deve

- inventar `actualDuration`;
- finalizar a sessão automaticamente;
- registrar questões que não foram informadas;
- modificar sessões anteriores.
