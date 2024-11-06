# Trabalhando com banco de dados - SQLite3

Aqui você encontra alguns trechos de códigos que podem ser usados para o começo de uma implementação!!

```python
import sqlite3

# Conexão com o banco SQLite
conn = sqlite3.connect('exemplo.db')
cursor = conn.cursor()

# Criando uma tabela
cursor.execute('''CREATE TABLE IF NOT EXISTS alunos (id INTEGER PRIMARY KEY, nome TEXT, idade INTEGER)''')
conn.commit()

# INSERT
cursor.execute("INSERT INTO alunos (nome, idade) VALUES (?, ?)", ('Maria', 20))
conn.commit()

# SELECT
cursor.execute("SELECT * FROM alunos")
result = cursor.fetchall()
print("Select Result:", result)

# UPDATE
cursor.execute("UPDATE alunos SET idade = ? WHERE nome = ?", (21, 'Maria'))
conn.commit()

# DELETE
cursor.execute("DELETE FROM alunos WHERE nome = ?", ('Maria',))
conn.commit()

# Fechando a conexão
conn.close()
```
