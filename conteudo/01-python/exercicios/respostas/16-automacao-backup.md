# Resposta do Exercício 16 - Automação de backup

```python
import os
import shutil
from datetime import datetime

pasta_origem = '/caminho/para/pasta'
pasta_destino = '/caminho/para/backup'
nome_backup = f'backup_{datetime.now().strftime("%Y%m%d%H%M%S")}.zip'

shutil.make_archive(nome_backup.replace('.zip', ''), 'zip', pasta_origem)
shutil.move(nome_backup, os.path.join(pasta_destino, nome_backup))

print(f'Backup {nome_backup} criado com sucesso.')
```
