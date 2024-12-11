# Resposta do Exercício 4 - Gerenciamento de Usuários

```python
usuarios = [
    {'nome': 'Alice', 'permissao': 'admin'},
    {'nome': 'Bob', 'permissao': 'user'},
    {'nome': 'Carol', 'permissao': 'admin'}
]
for usuario in usuarios:
    if usuario['permissao'] == 'admin':
        print(f"Usuário admin: {usuario['nome']}")
```
