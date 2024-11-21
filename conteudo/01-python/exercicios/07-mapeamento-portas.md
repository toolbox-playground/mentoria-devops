# Mapeamento de Portas

## Cenário atual

Você está criando um script para ajudar os desenvolvedores do seu time a descobrir a porta que os principais serviços utilizam.
Para isso, considere a lista:
```
ssh: 22
http: 80
https: 443
dns: 53
rdp: 3389
```

Crie um script que dado o nome do serviço, ele retorne a porta que ele utiliza.

## Resultado esperado
Caso o serviço exista na sua lista:
```
O serviço <XPTO> utiliza a porta <XYZ>
```

Caso ele não exista:
```
Serviço não encontrado. Contate o administrador.
```

## Dica
Você pode utilizar a função *input* do Python para pedir para o usuário digitar algum valor.
