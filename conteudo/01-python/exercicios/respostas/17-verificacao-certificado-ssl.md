# Resposta do Exercício 17 - Verificação de Certificado SSL

```python
import ssl
import socket
import datetime

hostname = 'www.google.com'
context = ssl.create_default_context()
with socket.create_connection((hostname, 443)) as sock:
    with context.wrap_socket(sock, server_hostname=hostname) as ssock:
        cert = ssock.getpeercert()

data_expiracao = datetime.datetime.strptime(cert['notAfter'], '%b %d %H:%M:%S %Y %Z')
dias_restantes = (data_expiracao - datetime.datetime.now()).days

if dias_restantes > 0:
    print(f'O certificado SSL é válido por mais {dias_restantes} dias.')
else:
    print('O certificado SSL expirou.')
```
