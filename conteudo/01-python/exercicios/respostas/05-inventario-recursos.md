# Resposta do Exercício 5 - Inventário de Recursos

```python
inventario = {
    'CPU': (16, 'cores'),
    'Memória': (32, 'GB'),
    'Disco': (1, 'TB')
}
for recurso, detalhes in inventario.items():
    quantidade, unidade = detalhes
    print(f'{recurso}: {quantidade} {unidade}')
```
