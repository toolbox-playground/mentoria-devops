# Dicionários

## Definição

Os dicionários são coleções de pares **chave-valor**. São mutáveis e permitem o armazenamento de dados de forma associativa, onde cada chave única está vinculada a um valor.

# Criando um dicionário

```python
# Dicionário de configurações
configuracoes = {
    'host': 'localhost',
    'porta': 8080,
    'debug': True
}
```

## Principais características

- **Mutáveis:** Permitem adicionar, alterar ou remover pares chave-valor;
- **Chaves únicas:** Cada chave deve ser única dentro do dicionário;
- **Desordenados (até Python 3.6):** A partir do Python 3.7, mantém a ordem de inserção.

## Operações mais usadas

### Acessar valores
```python
host = configuracoes['host']
```

### Adicionar ou atualizar valores
```python
configuracoes['timeout'] = 30
```

### Remover pares chave-valor
```python
del configuracoes['debug']
```

### Iterar sobre chaves e valores
```python
for chave, valor in configuracoes.items():
    print(f'{chave}: {valor}')
```

## Alguns usos em DevOps
- Armazenar configurações de sistemas e aplicações.
- Mapear recursos, como servidores e seus atributos.
- Gerenciar inventários de infraestruturas.
