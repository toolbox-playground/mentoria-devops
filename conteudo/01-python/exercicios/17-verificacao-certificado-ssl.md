# Verificação de Certificados SSL

## Cenário Atual
Você acabou de passar por um incidente onde o certificado SSL do seu domínio expirou por falta de atenção!
Dessa forma, após uma longa discussão com o seu time sobre como poderiamos evitar isso no futuro, você decide criar um script que te reporta quantos dias faltam para o certificado expirar.

## Resultado esperado
Dado um determinado site, reporte quantos dias faltam para o certificado expirar.

## Dica
Existem as bibliotecas *ssl* e *socket* que podem te ajudar a fazer um request para um determinado site e retornar o seu certificado.
