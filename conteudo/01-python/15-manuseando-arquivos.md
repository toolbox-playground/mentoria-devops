# Exemplos de Manipulação de Arquivos CSV em Python

## Leitura de um arquivo CSV linha por linha

```python
import csv

with open("dados.csv", mode="r", newline="") as arquivo:
    leitor_csv = csv.reader(arquivo)
    for linha in leitor_csv:
        print(linha)
```

## Leitura de um arquivo CSV com cabeçalho usando `DictReader`

```python
import csv

with open("dados.csv", mode="r", newline="") as arquivo:
    leitor_csv = csv.DictReader(arquivo)
    for linha in leitor_csv:
        print(f"Nome: {linha['nome']}, Idade: {linha['idade']}")
```

## Escrita em um arquivo CSV usando `writer`

```python
import csv

dados = [
    ["nome", "idade", "cidade"],
    ["João", 28, "São Paulo"],
    ["Ana", 24, "Rio de Janeiro"],
    ["Carlos", 30, "Belo Horizonte"]
]

with open("saida.csv", mode="w", newline="") as arquivo:
    escritor_csv = csv.writer(arquivo)
    escritor_csv.writerows(dados)  # Escreve todas as linhas de uma vez
```

## Escrita em um arquivo CSV com cabeçalho usando `DictWriter`

```python
import csv

dados = [
    {"nome": "João", "idade": 28, "cidade": "São Paulo"},
    {"nome": "Ana", "idade": 24, "cidade": "Rio de Janeiro"},
    {"nome": "Carlos", "idade": 30, "cidade": "Belo Horizonte"}
]

with open("saida_com_cabecalho.csv", mode="w", newline="") as arquivo:
    cabecalho = ["nome", "idade", "cidade"]
    escritor_csv = csv.DictWriter(arquivo, fieldnames=cabecalho)
    escritor_csv.writeheader()  # Escreve o cabeçalho
    escritor_csv.writerows(dados)  # Escreve as linhas de dados
```

## Adicionando dados a um arquivo CSV existente (modo de apêndice)

```python
import csv

novos_dados = [
    ["Maria", 22, "Salvador"],
    ["Pedro", 35, "Fortaleza"]
]

with open("saida.csv", mode="a", newline="") as arquivo:
    escritor_csv = csv.writer(arquivo)
    escritor_csv.writerows(novos_dados)  # Adiciona novas linhas ao arquivo existente
```

## Leitura de um arquivo CSV e conversão para uma lista de dicionários

```python
import csv

dados = []
with open("dados.csv", mode="r", newline="") as arquivo:
    leitor_csv = csv.DictReader(arquivo)
    for linha in leitor_csv:
        dados.append(linha)

print(dados)
```

## Filtrando dados de um CSV ao ler

```python
import csv

with open("dados.csv", mode="r", newline="") as arquivo:
    leitor_csv = csv.DictReader(arquivo)
    for linha in leitor_csv:
        if int(linha["idade"]) > 25:  # Filtra pessoas com idade maior que 25
            print(linha)
```

## Modificando dados de um CSV e salvando em um novo arquivo

```python
import csv

dados_modificados = []
with open("dados.csv", mode="r", newline="") as arquivo:
    leitor_csv = csv.DictReader(arquivo)
    for linha in leitor_csv:
        linha["idade"] = int(linha["idade"]) + 1  # Aumenta a idade em 1
        dados_modificados.append(linha)

with open("dados_modificados.csv", mode="w", newline="") as arquivo:
    cabecalho = ["nome", "idade", "cidade"]
    escritor_csv = csv.DictWriter(arquivo, fieldnames=cabecalho)
    escritor_csv.writeheader()
    escritor_csv.writerows(dados_modificados)
```
