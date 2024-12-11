# Resposta do Exercício 7 - Mapeamento de Portas

```python
servicos = {'ssh': 22, 'http': 80, 'https': 443}
servico_input = input('Digite o nome do serviço: ')
porta = servicos.get(servico_input.lower())
if porta:
    print(f'O serviço {servico_input} utiliza a porta {porta}.')
else:
    print('Serviço não encontrado.')
```
