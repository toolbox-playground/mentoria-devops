# Exemplos com Tuplas em Python

## Criando uma tupla
```python
minha_tupla = (1, 2, 3, "Python")
print(minha_tupla)
```

## Acessando elementos de uma tupla
```python
minha_tupla = ("maçã", "banana", "laranja")
print(minha_tupla[1])  # Acessa o segundo elemento
```

## Desempacotando uma tupla
```python
frutas = ("maçã", "banana", "laranja")
fruta1, fruta2, fruta3 = frutas
print(fruta1)
print(fruta2)
print(fruta3)
```

## Iterando sobre uma tupla com `for`
```python
minha_tupla = (1, 2, 3)
for numero in minha_tupla:
    print(numero)
```

## Verificando a existência de um item em uma tupla
```python
minha_tupla = (1, 2, 3)
if 2 in minha_tupla:
    print("O número 2 está na tupla.")
```

---

# Exemplos com Dicionários em Python

## Criando um dicionário
```python
meu_dict = {"nome": "João", "idade": 25}
print(meu_dict)
```

## Acessando valores de um dicionário
```python
meu_dict = {"nome": "João", "idade": 25}
print(meu_dict["nome"])  # Acessa o valor associado à chave "nome"
```

## Adicionando e atualizando valores no dicionário
```python
meu_dict = {"nome": "João", "idade": 25}
meu_dict["cidade"] = "São Paulo"  # Adiciona nova chave-valor
meu_dict["idade"] = 26  # Atualiza o valor da chave "idade"
print(meu_dict)
```

## Iterando sobre um dicionário
```python
meu_dict = {"nome": "João", "idade": 25}
for chave, valor in meu_dict.items():
    print(f"{chave}: {valor}")
```

## Usando `get()` para acessar valores com valor padrão
```python
meu_dict = {"nome": "João", "idade": 25}
cidade = meu_dict.get("cidade", "Desconhecida")  # Retorna "Desconhecida" se "cidade" não existir
print(cidade)
```

## Removendo um item com `pop()`
```python
meu_dict = {"nome": "João", "idade": 25}
meu_dict.pop("idade")  # Remove a chave "idade"
print(meu_dict)
```

---

# Exemplos com Conjuntos em Python

## Criando um conjunto
```python
meu_set = {1, 2, 3}
print(meu_set)
```

## Adicionando elementos a um conjunto
```python
meu_set = {1, 2, 3}
meu_set.add(4)  # Adiciona o elemento 4 ao conjunto
print(meu_set)
```

## Removendo elementos de um conjunto
```python
meu_set = {1, 2, 3}
meu_set.discard(2)  # Remove o elemento 2, se ele existir
print(meu_set)
```

## União de dois conjuntos
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
uniao = set1 | set2  # Também pode usar set1.union(set2)
print(uniao)
```

## Interseção de dois conjuntos
```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}
intersecao = set1 & set2  # Também pode usar set1.intersection(set2)
print(intersecao)
```

## Diferença entre dois conjuntos
```python
set1 = {1, 2, 3}
set2 = {2, 3, 4}
diferenca = set1 - set2  # Elementos que estão em set1 mas não em set2
print(diferenca)
```

## Verificando a existência de um elemento no conjunto
```python
meu_set = {1, 2, 3}
if 2 in meu_set:
    print("O número 2 está no conjunto.")
```
