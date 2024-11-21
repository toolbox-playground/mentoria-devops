# Implementação de Retry com Exponential Backoff

## Cenário Atual
Você quer melhorar o seu script de monitoramento de sites para garantir que a sua monitoração é mais eficiente e não falhe por qualquer motivo.
Dessa forma, você decide adicionar algumas melhoras nesse script como:
- Numero de tentativas parametrizado
- Mecanismo de retry que incrementa 2 segundos a cada request que falhou

## Resultado esperado
Script que dado um determinado endereço web, faça um request para ele e mostre uma mensagem de sucesso na tela.
Em caso de falha, ele deve tentar novamente até alcançar o parametro de tentativas que você definiu anteriomente e, a cada tentativa ele deve espera 2 segundos antes de tentar novamente.

## Dica
Utiliza a lib *requests* para fazer um request para o site https://api.github.com, a fim de ter um exemplo.
