# Resposta do Exercício 12 - Monitoramento de site

```python
import requests

with open('urls.txt', 'r') as file:
    urls = file.readlines()

with open('resultados.txt', 'w') as output:
    for url in urls:
        url = url.strip()
        try:
            response = requests.get(url, timeout=5)
            if response.status_code == 200:
                output.write(f'{url} está online.\n')
            else:
                output.write(f'{url} retornou status {response.status_code}.\n')
        except requests.RequestException as e:
            output.write(f'{url} não está acessível. Erro: {e}\n')
```
