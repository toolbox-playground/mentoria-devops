# Trabalhando com banco de dados - PostgreSQL

Aqui você encontra alguns trechos de códigos que podem ser usados para o começo de uma implementação!!

## Instalação da dependência
Esse código utiliza um biblioteca externa, dessa forma, para fazer a instalção, execute:
```python
pip install psycopg2
```

## Exemplo para PostgreSQL
```python
import psycopg2

# Conexão com o banco PostgreSQL
conn = psycopg2.connect(
    host="localhost",
    user="seu_usuario",
    password="sua_senha",
    database="seu_banco"
)
cursor = conn.cursor()

# Criando uma tabela
cursor.execute("CREATE TABLE IF NOT EXISTS alunos (id SERIAL PRIMARY KEY, nome VARCHAR(255), idade INT)")
conn.commit()

# INSERT
cursor.execute("INSERT INTO alunos (nome, idade) VALUES (%s, %s)", ('Carlos', 30))
conn.commit()

# SELECT
cursor.execute("SELECT * FROM alunos")
result = cursor.fetchall()
print("Select Result:", result)

# UPDATE
cursor.execute("UPDATE alunos SET idade = %s WHERE nome = %s", (31, 'Carlos'))
conn.commit()

# DELETE
cursor.execute("DELETE FROM alunos WHERE nome = %s", ('Carlos',))
conn.commit()

# Fechando a conexão
conn.close()
```
