# Tuplas

## Definição

Uma tupla é uma coleção ordenada e imutável de elementos em Python (Isso significa que, após serem criadas, seus elementos não podem ser alterados). Elas são definidas usando parênteses **()** e os itens são separados por vírgulas.

## Criando uma tupla

```python
# Tupla Simples
tupla_exemplo = (1, 2, 3)

# Tupla com tipos mistos
tupla_mista = ('Servidor1', 8080, True)
```

## Principais características

- **Imutáveis:** Após criada, uma tupla não pode ser alterada (não é possível adicionar, remover ou modificar seus elementos);
- **Ordenadas:** Os itens têm uma ordem definida que não muda;
- **Tipos Diversos:** Podem conter elementos de diferentes tipos de dados (inteiros, strings, etc.).

## Operações mais usadas

### Acessar elementos
```python
primeiro_elemento = tupla_exemplo[0]
```

### Descompactação de tuplas
```python
a, b, c = tupla_exemplo
```

### Concatenar tuplas
```python
tupla_concatenada = tupla_exemplo + tupla_mista
```

## Alguns usos em DevOps
- Armazenar configurações padrão que não devem ser modificadas;
- Manter registros constantes, como códigos de status ou tipos de erros.
