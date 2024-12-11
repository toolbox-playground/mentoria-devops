# Resposta do Exercício 9 - Filtradem de Logs

```python
logs = [
    {'mensagem': 'Falha ao conectar', 'nivel': 'ERROR'},
    {'mensagem': 'Conexão estabelecida', 'nivel': 'INFO'},
    {'mensagem': 'Timeout', 'nivel': 'ERROR'}
]
erros = [log for log in logs if log['nivel'] == 'ERROR']
for erro in erros:
    print(erro['mensagem'])
```
