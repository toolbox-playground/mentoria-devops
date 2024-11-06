# Exemplos do Comando `if` e `elif` em Python

## `if` com `elif` e `else` 1
```python
x = 18
if x > 8:
	print("x é maior que 8")
elif x > 0:
	print("x é positivo")
else:
print("x é negativo")
```

## `if` com `elif` e `else` 2
```python
nota = 7
if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Bom")
else:
    print("Precisa melhorar")
```

## `if` com um único `elif`
```python
nota = 8
if nota >= 9:
    print("Excelente")
elif nota >= 7:
    print("Bom")
```

## `if` com múltiplos `elif`
```python
idade = 45
if idade < 12:
    print("Criança")
elif idade < 18:
    print("Adolescente")
elif idade < 60:
    print("Adulto")
else:
    print("Idoso")
```

## `if`, `elif` e `else` para cobrir todos os casos
```python
temperatura = 15
if temperatura > 30:
    print("Dia quente")
elif temperatura > 20:
    print("Dia agradável")
elif temperatura > 10:
    print("Dia frio")
else:
    print("Dia muito frio")
```

## `if` com `elif` usando operadores lógicos (`and`)
```python
hora = 14
if hora < 12:
    print("Bom dia")
elif hora >= 12 and hora < 18:
    print("Boa tarde")
else:
    print("Boa noite")
```

## `if` com `elif` usando condições complexas
```python
idade = 20
ingresso_vip = True

if idade < 18:
    print("Menor de idade")
elif idade >= 18 and not ingresso_vip:
    print("Adulto com ingresso padrão")
elif idade >= 18 and ingresso_vip:
    print("Adulto com ingresso VIP")
```

## `if` e `elif` em uma condição de classificação
```python
media = 7.5
if media >= 9:
    print("Aprovado com Distinção")
elif media >= 7:
    print("Aprovado")
elif media >= 5:
    print("Recuperação")
else:
    print("Reprovado")
```
