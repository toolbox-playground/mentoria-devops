# Resposta do Exercício 15 - Envio de Alerta via Email
```python
import psutil
import time

while True:
    uso_cpu = psutil.cpu_percent(interval=1)
    if uso_cpu > 80:
        print(f'Alerta! Uso de CPU alto: {uso_cpu}%')
        # Aqui você poderia implementar o envio de email
    time.sleep(5)
```
