# Resposta do Exercício 3 - Logs com Erros

```python
erros_criticos = ('500', '501', '502')
def verificar_erro(codigo_erro):
    if codigo_erro in erros_criticos:
        print(f'Erro crítico detectado: {codigo_erro}')
    else:
        print('Erro não crítico.')
```
