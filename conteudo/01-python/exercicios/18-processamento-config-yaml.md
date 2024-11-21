# Processamento de Configurações YAML

## Cenário Atual
As configurações dos seus servidores estão padronizadas através de um arquivo no formato YAML.
Porém, devido a uma mudança no endereço do banco de dados, você precisa criar um script que leia esse arquivo YAML e altere o endereço do banco de dados para *192.168.252.252*.

Detalhe, o seu arquivo de configuração se resume á:
```yaml
configuracoes = {
    'host': 'localhost',
    'porta': 8080,
    'debug': True,
    'database': {
        'engine': 'postgresql',
        'nome': 'meu_banco',
        'usuario': 'admin',
        'senha': 'senha_secreta',
        'host': 'db.local',
        'porta': 5432
    },
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
    'limites': {
        'conexoes_maximas': 100,
        'threads': 4,
        'tempo_timeout': 30
    },
    'recursos': ('CPU', 'Memória', 'Disco'),
    'ambiente': 'produção',
    'seguranca': {
        'csrf_protection': True,
        'allowed_hosts': ['localhost', 'meusite.com'],
        'csp': "default-src 'self'; script-src 'self' 'unsafe-inline';"
    },
    'emails': {
        'suporte': 'suporte@meusite.com',
        'no-reply': 'no-reply@meusite.com'
    },
    'enderecos_ip': ['192.168.1.1', '192.168.1.2', '192.168.1.3'],
    'feature_flags': {
        'novo_layout': False,
        'beta_teste': True
    },
    'api_keys': {
        'servico_externo': 'abcdef1234567890'
    }
}
```

## Resultado esperado
Dado o arquivo de configuração acima, a chave *host* do database precisa ser alterada via script Python.

## Dica
Você pode utilizar a lib *yaml* para facilitar a sua vida.
