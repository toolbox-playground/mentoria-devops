# Exmplos de como utilizar a função print()

## Exibindo uma mensagem de texto
```python
print("Hello World")
```

## Exibindo variáveis em mensagens
```python
nome = "João Heytor"
idade = 38
print("Me chamo ", nome, "e tenho ", idade, "anos de idade")
```

```python
nome = "João Heytor"
idade = 38
print("Me chamo ", nome, " e tenho ", idade, " anos de idade", sep="-")
```

```python
print("Hello World", end=" COM PYTHON")
```

```python
nome = "João Heytor"
idade = 38
print("Me chamo {}  e tenho {} anos de idade".format(nome, idade))
```

## 3. Interpolação de Strings (f-strings)
```python
nome = "João Heytor"
idade = 38
print(f"Me chamo {nome} e tenho {idade} anos de idade")
```
