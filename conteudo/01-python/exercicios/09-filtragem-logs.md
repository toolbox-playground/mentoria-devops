# Filtragem de Logs

## Cenário Atual
Você está investigando um problema em produção que causou um grande incidente na principal aplicação da sua empresa. Após se conectar ao servidor, você pegou o arquivo de logs que se resume a:
```
'mensagem': 'Falha ao conectar ao servidor', 'nivel': 'ERROR'
'mensagem': 'Conexao estabelecida', 'nivel': 'INFO'
'mensagem': 'Timeout', 'nivel': 'ERROR'
'mensagem': 'Falha ao conectar ao servidor', 'nivel': 'ERROR'
'mensagem': 'Timeout', 'nivel': 'ERROR'
```

O problema é crítico e você precisa criar uma forma de mostrar apenas os logs que possuem a severidade 'ERROR'.

## Resultado esperado
```
'mensagem': 'XPTO', 'nivel': 'ERROR'
'mensagem': 'XPTO', 'nivel': 'ERROR'
...
```

## Dica
É possível colocar todos os logs em uma lista e depois usar a combinação de iteração com estrutura de decisão.
