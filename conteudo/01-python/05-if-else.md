# Exemplos de como utilizar o `if-else`

## `if` com `else`
```python
idade = 16
if idade >= 18:
    print("Você é maior de idade.")
else:
    print("Você é menor de idade.")
```

## `if` com operadores lógicos (`and`)
```python
idade = 25
habilitacao = True

if idade >= 18 and habilitacao:
    print("Você pode dirigir.")
else:
    print("Não autorizado a dirigir.")
```

## `if` com operadores lógicos (`or`)
```python
tem_carteirinha = False
tem_convite = True

if tem_carteirinha or tem_convite:
    print("Você pode entrar no evento.")
else:
    print("Entrada não permitida.")
```

## `if` com operador `not`
```python
chovendo = False

if not chovendo:
    print("Pode sair sem guarda-chuva.")
else:
    print("Leve o guarda-chuva.")
```

## `if` com comparação de strings
```python
senha = "Python123"
if senha == "Python123":
    print("Acesso concedido.")
else:
    print("Senha incorreta.")
```
