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

## Alguns benefícios das tuplas para devops
### Imutabilidade Garantida
- Proteção de Dados Sensíveis: Tuplas são imutáveis, o que significa que, após a criação, seus valores não podem ser alterados. Isso é útil para armazenar configurações ou constantes que não devem ser modificadas durante a execução do script, garantindo a integridade dos dados;
- Confiabilidade em Ambientes Críticos: Em scripts de automação que interagem com sistemas de produção, a imutabilidade previne alterações acidentais que poderiam causar falhas ou comportamentos indesejados.

### Desempenho Melhorado
- Operações Mais Rápidas: Tuplas podem ser mais eficientes que listas em termos de desempenho, especialmente em operações de leitura, devido à sua natureza imutável;
- Menor Sobrecarga de Memória: Como são imutáveis, o Python pode otimizar o armazenamento de tuplas, resultando em menor uso de memória, o que é benéfico em scripts que lidam com grandes volumes de dados.

### Uso como Chaves em Dicionários
- Chaves Imutáveis: Tuplas podem ser usadas como chaves em dicionários (desde que contenham apenas elementos imutáveis), permitindo a criação de estruturas de dados complexas que mapeiam combinações de valores para resultados ou configurações específicas;
- Indexação Avançada: Isso é útil em casos onde múltiplos atributos precisam ser combinados para formar uma chave única, facilitando a recuperação de dados.

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
