# Resposta do Exercício 11 - Consulta status de API

```python
import requests

response = requests.get('https://www.githubstatus.com/api/v2/status.json')
if response.status_code == 200:
    data = response.json()
    status = data['status']['description']
    print(f'Status do GitHub: {status}')
else:
    print('Não foi possível obter o status do GitHub.')
````
