# Envio de Alertas por Email

## Cenário Atual
Você quer ser pró-ativo para identificar quando possíveis problemas podem surgir.
Para começar, você decide criar um script que monitore a CPU a cada 5 segundos, caso o uso de CPU seja maior do que 80%, você decide imprimir o valor na tela.

## Resultado esperado
```
Alerta! Uso do CPU alto: XPTO%
```

# Dica
Existe duas bibliotecas no Python que podem te ajudar:
```
**- psutil:** Consegue ler alguns dados do seu sistema, como a CPU
**- time:** Te permite utilizar algumas funções relacionado a tempo, como o *sleep*.
