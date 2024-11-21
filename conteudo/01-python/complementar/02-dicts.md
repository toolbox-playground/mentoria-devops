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
    'log': {
        'nivel': 'INFO',
        'arquivo': '/var/log/aplicacao.log',
        'rotacao': 'diaria',
        'formato': '%(asctime)s - %(levelname)s - %(message)s'
    },
    'servicos_ativos': ['auth', 'api', 'web'],
    'versao': '1.2.3',
    'plugins': {
        'cache': {
            'ativo': True,
            'tipo': 'redis',
            'host': 'cache.local',
            'porta': 6379
        },
        'monitoramento': {
            'ativo': False
        }
    },
    'api_keys': {
        'servico_externo': 'abcdef1234567890'
    }
}
```

## Principais características

- **Mutáveis:** Permitem adicionar, alterar ou remover pares chave-valor;
- **Chaves únicas:** Cada chave deve ser única dentro do dicionário;
- **Desordenados (até Python 3.6):** A partir do Python 3.7, mantém a ordem de inserção.

## Alguns benefícios de um dicionário para devops

### Organização de Dados Complexos
Dicionários permitem armazenar dados em pares chave-valor, facilitando a representação de configurações complexas, credenciais, parâmetros e outras informações estruturadas necessárias em tarefas de DevOps.

### Acesso Rápido a Dados
Com chaves únicas, é possível acessar rapidamente valores específicos sem a necessidade de percorrer toda a estrutura de dados. Isso é útil ao manipular grandes conjuntos de configurações ou dados de estado.

### Mutabilidade e Flexibilidade
Dicionários são mutáveis, permitindo adicionar, atualizar ou remover pares chave-valor conforme necessário durante a execução de scripts ou aplicações. Isso é essencial em ambientes onde as configurações podem mudar dinamicamente.

### Representação de Configurações Hierárquicas
Suportam aninhamento, permitindo representar configurações hierárquicas e complexas, como arquivos YAML ou JSON, que são comumente usados em DevOps para configurar aplicações e infraestrutura.

### Integração com APIs e Serviços Web
Ao trabalhar com APIs que utilizam JSON, dicionários são fundamentais para construir e interpretar payloads, facilitando a comunicação entre serviços.

### Facilita a Automatização de Tarefas
Ao manipular configurações e dados programaticamente, é possível automatizar tarefas como deploys, provisionamento de recursos e gerenciamento de infraestrutura.

### Melhora a Legibilidade e Manutenção do Código
O uso de chaves descritivas torna o código mais legível e fácil de manter, o que é crucial em equipes DevOps colaborativas.

### Manipulação Dinâmica de Dados
Permite carregar, modificar e salvar configurações em tempo de execução, adaptando-se a diferentes ambientes (desenvolvimento, teste, produção) sem alterar o código fonte.

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
