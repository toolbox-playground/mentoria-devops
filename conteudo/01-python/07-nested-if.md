# Exemplos de `if` Aninhado (Nested `if`)

## Verificação de múltiplas condições com `if` aninhado
```python
idade = 20
tem_identidade = True

if idade >= 18:
    if tem_identidade:
        print("Entrada permitida.")
    else:
        print("É necessário apresentar uma identidade.")
else:
    print("Idade insuficiente para entrada.")
```

## `if` aninhado com `elif` e `else`
```python
nota = 8
frequencia = 85

if nota >= 7:
    if frequencia >= 75:
        print("Aprovado")
    else:
        print("Reprovado por frequência")
else:
    print("Reprovado por nota")
```

## `if` aninhado em um contexto de triagem
```python
idade = 30
experiencia = 5

if idade >= 18:
    if experiencia >= 3:
        print("Candidato qualificado")
    else:
        print("Experiência insuficiente")
else:
    print("Candidato menor de idade")
```

## `if` aninhado com múltiplos níveis
```python
dia_da_semana = "sábado"
hora = 14

if dia_da_semana == "sábado" or dia_da_semana == "domingo":
    if hora < 18:
        print("Atendimento disponível")
    else:
        print("Atendimento encerrado")
else:
    if hora >= 9 and hora < 18:
        print("Atendimento disponível")
    else:
        print("Fora do horário de atendimento")
```

## `if` aninhado para checar faixa de idade e permissão
```python
idade = 16
autorizacao_pais = True

if idade < 18:
    if autorizacao_pais:
        print("Autorizado com permissão dos pais")
    else:
        print("Permissão dos pais necessária")
else:
    print("Autorizado, maior de idade")
```

## `if` aninhado com `and` e `or` para condições combinadas
```python
idade = 25
ingresso_vip = False
membro_clube = True

if idade >= 18:
    if ingresso_vip or membro_clube:
        print("Acesso liberado à área VIP")
    else:
        print("Acesso permitido somente à área comum")
else:
    print("Acesso negado, menor de idade")
```
