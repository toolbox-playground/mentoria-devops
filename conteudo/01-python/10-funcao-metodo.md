# Exemplos de Funções

## Criando uma função simples
```python
def saudacao():
    print("Olá, seja bem-vindo!")

saudacao()
```

## Função com parâmetros
```python
def saudacao(nome):
    print(f"Olá, {nome}!")

saudacao("João")
```

## Função com valor de retorno
```python
def soma(a, b):
    return a + b

resultado = soma(3, 4)
print(resultado)
```

## Função com valor padrão para um parâmetro
```python
def saudacao(nome="Visitante"):
    print(f"Olá, {nome}!")

saudacao()          # Usa o valor padrão
saudacao("Ana")     # Sobrescreve o valor padrão
```

## Função com número variável de argumentos (`*args`)
```python
def soma(*numeros):
    total = sum(numeros)
    return total

print(soma(1, 2, 3, 4, 5))  # Soma todos os números passados
```

## Função com argumentos nomeados (`**kwargs`)
```python
def exibir_informacoes(**dados):
    for chave, valor in dados.items():
        print(f"{chave}: {valor}")

exibir_informacoes(nome="João", idade=30, cidade="São Paulo")
```

---

# Exemplos de Métodos

Métodos são funções definidas dentro de classes e que operam em instâncias de objetos.

## Criando uma classe com um método
```python
class Pessoa:
    def saudacao(self):
        print("Olá!")

p = Pessoa()
p.saudacao()
```

## Método com parâmetros
```python
class Pessoa:
    def apresentar(self, nome):
        print(f"Olá, meu nome é {nome}.")

p = Pessoa()
p.apresentar("João")
```

## Método que modifica o estado do objeto
```python
class Contador:
    def __init__(self):
        self.contagem = 0
    
    def incrementar(self):
        self.contagem += 1

c = Contador()
c.incrementar()
print(c.contagem)
```

---

# Exemplos de Classes

## Definindo uma classe com um atributo e um método
```python
class Carro:
    def __init__(self, marca):
        self.marca = marca
    
    def exibir_marca(self):
        print(f"A marca do carro é {self.marca}.")

meu_carro = Carro("Toyota")
meu_carro.exibir_marca()
```

## Classe com atributos privados e métodos de acesso
```python
class Banco:
    def __init__(self, saldo):
        self.__saldo = saldo  # Atributo privado
    
    def depositar(self, valor):
        self.__saldo += valor
    
    def consultar_saldo(self):
        print(f"Saldo atual: {self.__saldo}")

conta = Banco(1000)
conta.depositar(500)
conta.consultar_saldo()
```

## Classe com herança
```python
class Animal:
    def falar(self):
        print("O animal faz um som")

class Cachorro(Animal):
    def falar(self):
        print("O cachorro late")

meu_cachorro = Cachorro()
meu_cachorro.falar()  # Sobrescreve o método da classe pai
```

## Classe com métodos estáticos
```python
class Matematica:
    @staticmethod
    def soma(a, b):
        return a + b

resultado = Matematica.soma(3, 5)
print(resultado)
```

## Classe com métodos de classe
```python
class Pessoa:
    populacao = 0
    
    def __init__(self, nome):
        self.nome = nome
        Pessoa.populacao += 1
    
    @classmethod
    def exibir_populacao(cls):
        print(f"População total: {cls.populacao}")

p1 = Pessoa("Ana")
p2 = Pessoa("João")
Pessoa.exibir_populacao()
```
