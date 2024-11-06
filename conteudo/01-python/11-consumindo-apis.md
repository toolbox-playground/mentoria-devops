# Exemplos de Consumo de APIs com `requests` em Python

## Realizando uma Requisição GET Simples

```python
import requests

url = "https://api.exemplo.com/dados"
response = requests.get(url)

if response.status_code == 200:
    dados = response.json()  # Converte a resposta para JSON
    print(dados)
else:
    print("Falha na requisição:", response.status_code)
```

## Requisição GET com Parâmetros

```python
import requests

url = "https://api.exemplo.com/pesquisa"
parametros = {"query": "Python", "limite": 10}

response = requests.get(url, params=parametros)

if response.status_code == 200:
    dados = response.json()
    print(dados)
else:
    print("Falha na requisição:", response.status_code)
```

## Requisição POST com Dados JSON

```python
import requests

url = "https://api.exemplo.com/usuarios"
dados = {
    "nome": "João",
    "idade": 30,
    "cidade": "São Paulo"
}

response = requests.post(url, json=dados)

if response.status_code == 201:  # Código 201 indica criação bem-sucedida
    print("Usuário criado com sucesso:", response.json())
else:
    print("Erro ao criar usuário:", response.status_code)
```

## Enviando Dados em Formulário com POST

```python
import requests

url = "https://api.exemplo.com/login"
dados = {"usuario": "joao", "senha": "minha_senha"}

response = requests.post(url, data=dados)

if response.status_code == 200:
    print("Login realizado com sucesso")
else:
    print("Falha no login:", response.status_code)
```

## Requisição PUT para Atualizar Dados

```python
import requests

url = "https://api.exemplo.com/usuarios/1"
dados = {"nome": "João Atualizado", "idade": 31}

response = requests.put(url, json=dados)

if response.status_code == 200:
    print("Dados atualizados com sucesso:", response.json())
else:
    print("Erro ao atualizar dados:", response.status_code)
```

## Requisição DELETE para Remover um Recurso

```python
import requests

url = "https://api.exemplo.com/usuarios/1"
response = requests.delete(url)

if response.status_code == 204:  # Código 204 indica exclusão bem-sucedida
    print("Usuário excluído com sucesso")
else:
    print("Erro ao excluir usuário:", response.status_code)
```

## Usando Headers para Autenticação com Token

```python
import requests

url = "https://api.exemplo.com/dados"
headers = {"Authorization": "Bearer SEU_TOKEN_AQUI"}

response = requests.get(url, headers=headers)

if response.status_code == 200:
    dados = response.json()
    print(dados)
else:
    print("Falha na autenticação:", response.status_code)
```

## Tratando Erros com `try` e `except`

```python
import requests

url = "https://api.exemplo.com/dados"

try:
    response = requests.get(url)
    response.raise_for_status()  # Lança uma exceção para códigos de erro HTTP
    dados = response.json()
    print(dados)
except requests.exceptions.HTTPError as err:
    print("Erro HTTP:", err)
except requests.exceptions.RequestException as err:
    print("Erro na requisição:", err)
```

## Timeout para Requisição Lenta

```python
import requests

url = "https://api.exemplo.com/dados"

try:
    response = requests.get(url, timeout=5)  # Tempo limite de 5 segundos
    dados = response.json()
    print(dados)
except requests.exceptions.Timeout:
    print("A requisição demorou muito e foi interrompida.")
```

---
