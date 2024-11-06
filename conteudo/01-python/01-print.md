# Exemplos de como utilizar a função print()

## Exibindo uma mensagem de texto
```python
print("Hello World")
```

## Exibindo variáveis em uma mensagem python
```python
nome = "João Heytor"
idade = 38
print("Me chamo ", nome, "e tenho ", idade, "anos de idade")
```

## Personalizando o separador entre argumentos
```python
nome = "João Heytor"
idade = 38
print("Me chamo ", nome, " e tenho ", idade, " anos de idade", sep="-")
```

## Alterando o final da linha com end
```python
print("Hello World", end=" COM PYTHON")
```

## Usando .format() para formatar strings
```python
nome = "João Heytor"
idade = 38
print("Me chamo {}  e tenho {} anos de idade".format(nome, idade))
```

## Interpolação de Strings (f-strings)
```python
nome = "João Heytor"
idade = 38
print(f"Me chamo {nome} e tenho {idade} anos de idade")
```
