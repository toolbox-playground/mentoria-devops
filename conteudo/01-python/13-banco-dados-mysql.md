# Trabalhando com banco de dados - MySQL

Aqui você encontra alguns trechos de códigos que podem ser usados para o começo de uma implementação!!

## Instalação da dependência
Esse código utiliza um biblioteca externa, dessa forma, para fazer a instalção, execute:
```python
pip install mysql-connector-python
```

## Exemplo para MySQL
```python
import mysql.connector

# Conexão com o banco MySQL
conn = mysql.connector.connect(
    host="localhost",
    user="seu_usuario",
    password="sua_senha",
    database="seu_banco"
)
cursor = conn.cursor()

# Criando uma tabela
cursor.execute("CREATE TABLE IF NOT EXISTS alunos (id INT AUTO_INCREMENT PRIMARY KEY, nome VARCHAR(255), idade INT)")

# INSERT
cursor.execute("INSERT INTO alunos (nome, idade) VALUES (%s, %s)", ('João', 25))
conn.commit()

# SELECT
cursor.execute("SELECT * FROM alunos")
result = cursor.fetchall()
print("Select Result:", result)

# UPDATE
cursor.execute("UPDATE alunos SET idade = %s WHERE nome = %s", (26, 'João'))
conn.commit()

# DELETE
cursor.execute("DELETE FROM alunos WHERE nome = %s", ('João',))
conn.commit()

# Fechando a conexão
conn.close()
```

