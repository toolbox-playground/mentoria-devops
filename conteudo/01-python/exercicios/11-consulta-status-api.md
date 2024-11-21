# Consulta a API de Status de Serviço

## Cenário Atual

O **GitHub** é um serviço crucial para todo o seu processo de CI/CD e você tem sofrido com as inumeras reclamações dos seus clientes internos das inumeras quedas desse serviço.

Dessa forma, você decidiu crir um script de automação que monitore o site do Github e em caso de algum incidente, reporte isso nos principais canais da sua empresa.

Pesquisando pela internet, você descobriu que existe o site https://www.githubstatus.com, que é onde os engenheiros responsáveis pelo Github notificam os usuários em caso de qualquer problema.

Você também descobriu que existe um endpoint publico nesse site que pode facilitar a vida: https://www.githubstatus.com/api/v2/status.json. Esse endpoint te retorna um JSON com o status atual do serviço!

Dessa forma, precisamos fazer uma chamada para esse endereço e imprimir na tela qual o status atual do Github.

## Resultado esperado
```
Status do Github: XPTO
```

## Dica
Com a ajuda da lib *requests* é possível fazer uma chamada para um endereço web.
