# Resposta do Exercício 19 - Criação de Gráfico

```python
import psutil
import matplotlib.pyplot as plt
import time

uso_memoria = []
tempo = []

for i in range(10):
    uso = psutil.virtual_memory().percent
    uso_memoria.append(uso)
    tempo.append(i)
    time.sleep(1)

plt.plot(tempo, uso_memoria)
plt.xlabel('Tempo (s)')
plt.ylabel('Uso de Memória (%)')
plt.title('Uso de Memória nos Últimos 10 Segundos')
plt.show()
```
