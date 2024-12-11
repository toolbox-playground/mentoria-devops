# Resposta do Exercício 18 - Processamento de Config em Yaml

```python
import yaml

with open('config.yaml', 'r') as yaml_file:
    config = yaml.safe_load(yaml_file)

config['database']['host'] = 'novo_host'

with open('config.yaml', 'w') as yaml_file:
    yaml.dump(config, yaml_file)

print('Configuração atualizada com sucesso.')
```
