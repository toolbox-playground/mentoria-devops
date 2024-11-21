# Automatização de Backup

## Cenário Atual
Todos nós sabemos que o backup é algo crucial para nos ajudar em caso de desastres que podem ocorrer no nosso ecosistema.
Atualmente, você, manualmente, compacta um determinado diretório (*o diretório da sua aplicação*) e move esse arquivo para o seu storage de backup a fim de garantir que o mesmo está a salvo.

Querendo otimizar o seu tempo, você decide criar um arquivo que faça todo esse processo:
1 - Lê um determinado diretório;
2 - Faz a sua compactação;
3 - Move o arquivo compactado para outro diretório.

## Resultdo esperado
Arquivo compactado criado e salvo em um determinado diretório, além de uma mensagem de sucesso na tela.

## Dica
As bibliotecas *os* e *shutil* te ajudarão com esse exercício.
