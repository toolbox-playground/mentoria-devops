# Exemplos do Loop `while` 

## Estrutura básica do `while`
```python
contador = 1
while contador <= 5:
    print(f"Contagem: {contador}")
    contador += 1
```

## `while` com `else`
```python
contador = 1
while contador <= 3:
    print(f"Contagem: {contador}")
    contador += 1
else:
    print("Loop concluído")
```

## `while` com `break`
```python
contador = 1
while contador <= 5:
    print(f"Contagem: {contador}")
    if contador == 3:
        print("Interrompendo o loop")
        break
    contador += 1
```

## `while` com `continue`
```python
contador = 0
while contador < 5:
    contador += 1
    if contador == 3:
        print("Pulando o número 3")
        continue
    print(f"Número: {contador}")
```

## `while` com `pass` (loop vazio)
```python
contador = 1
while contador <= 3:
    pass  # Mantém o loop vazio, sem realizar nenhuma ação
    contador += 1
print("Loop `while` vazio executado")
```

---

# Exemplos do Loop `for`

## Estrutura básica do `for` com listas
```python
frutas = ["maçã", "banana", "laranja"]
for fruta in frutas:
    print(f"Fruta: {fruta}")
```

## `for` com `range()`
```python
for i in range(5):
    print(f"Contagem: {i}")
```

## `for` com `else`
```python
for i in range(3):
    print(f"Valor: {i}")
else:
    print("Loop concluído")
```

## `for` com `break`
```python
for i in range(5):
    if i == 3:
        print("Interrompendo o loop")
        break
    print(f"Valor: {i}")
```

## `for` com `continue`
```python
for i in range(5):
    if i == 2:
        print("Pulando o número 2")
        continue
    print(f"Valor: {i}")
```

## `for` com `pass` (loop vazio)
```python
numeros = [1, 2, 3]
for numero in numeros:
    pass  # Loop vazio, nenhuma ação é realizada
print("Loop `for` vazio executado")
```
