# Resposta do Exercício 10 - Atualização de Inventário

```python
estoque = {'RAM': 10, 'SSD': 5, 'CPU': 2}
componente = input('Digite o componente: ')
quantidade_vendida = int(input('Quantidade vendida: '))
if componente in estoque:
    estoque[componente] -= quantidade_vendida
else:
    estoque[componente] = -quantidade_vendida
print(f'Estoque atualizado: {estoque}')
```
