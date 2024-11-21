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

## Alguns benefícios de uma lista para devops
### Armazenamento Ordenado de Dados Mutáveis
- Flexibilidade na Manipulação: Listas permitem adicionar, remover e modificar elementos, tornando-as ideais para situações onde os dados precisam ser atualizados dinamicamente;
- Preservação da Ordem: Mantêm a ordem de inserção dos elementos, o que é útil para processar dados sequencialmente, como filas de tarefas ou etapas de um pipeline de deploy.

### Facilidade na Iteração e Processamento em Lote
- Operações em Conjuntos de Dados: Permite iterar facilmente sobre elementos para aplicar operações em lote, como verificar o status de múltiplos servidores ou serviços;
- List Comprehensions: Facilita a criação de novas listas baseadas em condições ou transformações dos elementos existentes, aumentando a eficiência e legibilidade do código.

### Operações de Pilha e Fila
- Estruturas de Dados Lineares: Listas podem ser usadas como pilhas (LIFO) ou filas (FIFO) com métodos como append(), pop(), insert(), facilitando o controle de fluxos de trabalho;
- Gerenciamento de Tarefas: Útil para implementar sistemas simples de enfileiramento ou agendamento de tarefas em scripts de automação.

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
