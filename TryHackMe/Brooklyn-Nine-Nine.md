
# Desafio realizado em Brooklyn Nine-Nine

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/bca68343-88b1-4090-96b1-d396bf011b70)

Como inicio de todo CTF, primeiro temos que começar com o reconhecimento,nesse caso vamos começar com o NMAP

## NMAP
comando utilizado == nmap -v -sSV -sC <IP>

Com isso tivemos esse retorno

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/c02a195f-29b2-4a01-9d20-ec2f7b964b93)

Vemos que, temos 3 por abertas, 21, 22 e 80. Como o proprio NMAP ja retornou, o FTP temos como acessar via anonymous, então vamos verificar o que pode conter la.

## FTP
