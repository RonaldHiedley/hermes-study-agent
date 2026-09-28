# Teste: end-session

## Objetivo

Verificar a finalização correta de uma sessão.

## Pré-condição

Existe uma sessão em andamento com:

- plannedDuration: 45 min
- questionsAttempted: 8
- correct: 6

## Entrada

End session

## Resultado esperado

O Hermes deve:

- registrar automaticamente o horário de término;
- calcular `actualDuration` a partir dos horários;
- preservar `plannedDuration: 45 min`;
- calcular `accuracy: 75%`;
- apresentar os dados antes da confirmação;
- salvar a sessão somente após confirmação.

## Regra especial

Se o usuário informar explicitamente quanto tempo estudou, por exemplo:

"Estudei efetivamente 40 minutos."

então:

- `actualDuration = 40 min`;
- `plannedDuration` continua sendo 45 min;
- o valor informado pelo usuário prevalece sobre o cálculo automático.

## Não deve

- transformar 45 min planejados em 45 min reais;
- substituir `actualDuration` por `plannedDuration`;
- salvar sem confirmação.
