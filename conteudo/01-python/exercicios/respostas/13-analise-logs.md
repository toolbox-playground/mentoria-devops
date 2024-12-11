# Resposta do Exercício 13 - Análise de Logs 2

```python
from collections import Counter

with open('access.log', 'r') as log_file:
    ips = [line.split()[0] for line in log_file]

contagem_ips = Counter(ips)
top_5_ips = contagem_ips.most_common(5)

for ip, count in top_5_ips:
    print(f'{ip}: {count} vezes')
```
