# Resposta do Exercício 20 - Retry com Exponencial

```python
import requests
import time

def requisicao_com_retry(url, tentativas=5):
    atraso = 1
    for tentativa in range(tentativas):
        try:
            response = requests.get(url, timeout=5)
            if response.status_code == 200:
                return response
            else:
                print(f'Status code {response.status_code}. Tentando novamente...')
        except requests.RequestException as e:
            print(f'Erro: {e}. Tentativa {tentativa + 1} de {tentativas}.')
        time.sleep(atraso)
        atraso *= 2
    return None

resposta = requisicao_com_retry('https://api.github.com')
if resposta:
    print('Requisição bem-sucedida.')
else:
    print('Falha após várias tentativas.')
```
