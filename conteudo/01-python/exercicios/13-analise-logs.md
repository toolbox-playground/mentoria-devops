# Análise de Logs

## Cenário Atual
Você recebeu uma demanda do time de segurança para reportar quais são os Top5 IPs que mais acessam um determinado site.
Após se conectar ao seu servidor web, você pegou o arquivo access.log, que contem todos os acessos efetuados ao sistema.

Dessa forma, você precisa pegar esse arquivo e imprimir os 5 endereços de IP que mais acessaram o nosso site.

## Resultado esperado
```
IP: X vezes
IP: Y vezes
...
```

# Dicas
Você sabe que o arquivo access.logo do seu webserver segue o formato:
```
192.168.1.1 - - [20/Nov/2024:12:00:00 +0000] "GET /index.html HTTP/1.1" 200 1024
192.168.1.2 - - [20/Nov/2024:12:01:00 +0000] "GET /about.html HTTP/1.1" 200 512
```
Ou seja, o IP é o primeiro elemento de cada linha.

Existe uma lib que pode ser usada para agrupar determinados padrões:
```python
from collections import Counter
```

Mais detalhes na documentação oficial: https://docs.python.org/3/library/collections.html
