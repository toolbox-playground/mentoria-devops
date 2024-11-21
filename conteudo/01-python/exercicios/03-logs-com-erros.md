# Logs de Erro

## Cenário Atual

Você está trabalhando em um script de monitoração para as aplicações internas da sua empresa. Para isso, você precisa verificar se os erros:
```
500
501
502
503
```

Estão disponíveis na sua lista de monitoramento!

Considere uma tupla imutável que contém os códigos de erro críticos ('500', '501', '502'). Escreva uma função que verifica se um código de erro está na lista de erros críticos.

## Resultado esperado
Caso o código de erro exista na sua lista:
```
Erro critico detectado: 501
```

Se o erro não existir:
```
Erro não crítico.
```

## Dica
Tuplas com uma estrutura de decisão podem te ajudar nisso
