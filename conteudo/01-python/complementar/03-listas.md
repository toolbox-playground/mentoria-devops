# Listas

## Definição

As listas são coleções ordenadas e mutáveis de elementos. São definidas usando colchetes **[]** e podem conter elementos de diferentes tipos de dados.

# Criando uma lista
```python
# Lista de servidores
servidores = ['Servidor1', 'Servidor2', 'Servidor3']
```

## Principais características

- **Mutáveis:** Permitem adicionar, remover ou alterar elementos;
- **Ordenadas:** Mantêm a ordem de inserção dos elementos;
- **Indexadas:** Elementos acessíveis por índices.

## Operações mais usadas

### Acessar Elementos
```python
primeiro_servidor = servidores[0]  # Saída: 'Servidor1'
```

### Adicionar Elementos
```python
servidores.append('Servidor4')
```

### Inserir elementos em uma posição específica
```python
servidores.insert(1, 'ServidorNovo')
```

### Remover elementos
```python
servidores.remove('Servidor2')
```

### Iterar sobre a lista
```python
for servidor in servidores:
    print(servidor)
```

## Alguns usos em DevOps
- Gerenciar listas de tarefas ou processos em execução;
- Armazenar sequências de comandos ou etapas de deploy;
- Manipular coleções de dados, como resultados de consultas.
