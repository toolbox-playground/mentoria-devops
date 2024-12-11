# Resposta do Exercício 14 - Upload de Arquivos

```python
import requests

url = 'https://httpbin.org/post'
files = {'arquivo': open('documento.txt', 'rb')}

response = requests.post(url, files=files)
if response.status_code == 200:
    print('Upload realizado com sucesso.')
else:
    print('Falha no upload.')
```
