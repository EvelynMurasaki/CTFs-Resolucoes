
# Desafio realizado em Brooklyn Nine-Nine
Eu acredito que esse desafio tem duas formas de resolver, entao iremos pelo caminho 1 e o mais rapido que eu considero

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/bca68343-88b1-4090-96b1-d396bf011b70)

Como inicio de todo CTF, primeiro temos que começar com o reconhecimento, nesse caso vamos começar com o NMAP

## CAMINHO 01 - Com JAKE
## NMAP
comando utilizado == nmap -v -sSV -sC < IP >

Com isso tivemos esse retorno

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/c02a195f-29b2-4a01-9d20-ec2f7b964b93)

Vemos que, temos 3 por abertas, 21, 22 e 80. Como o proprio NMAP ja retornou, o FTP temos como acessar via anonymous, então vamos verificar o que pode conter la.

## FTP

comando utilizado == ftp anonymous@< IP > 21

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/f2d29800-d661-4e33-b2f6-f3347e9ae793)

Como podemos observar no recado da Amy pediu para o Jake trocar a senha, com isso temos ja nome de 2 usuarios para fazer o proximo passo que é ataque de força bruta

## BRUTE FORCE

Iremos utilizar a ferramenta Hydra

comando utilizado == hydra -l jake -P rockyou.txt < IP > ssh

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/863ef9ed-06fb-44a7-b576-c1768716b729)

Show demais, agora conseguimos a senha do Jake, ideia é testar o SSH agora.

## SSH

Parte para inicio da exploração

comando utilizado para conectar ==  ssh jake@< IP > 

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/ef7d4815-43ed-47f2-8a8b-f9189afacb29)

Hora de explorar e encontrar a primeira flag

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/9aa3e3d5-4eb4-4db3-95e0-0f4fea182def)

BOOM!

## ESCALA DE PRIVILEGIO

Primeiro passo, verificar se temos algum privilegio de root em algum lugar com o comando sudo -l

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/6ff215cb-cd63-428a-a72a-ea612ee5a3f9)

parece que temos em /usr/bin/less

com isso, olhar um arquivo na internet como escalar para root atraves desse local

site: https://gtfobins.github.io/gtfobins/less/#sudo

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/586db12f-b370-41c0-8d08-1f00a39a4ea3)

Vamos tentar.

comando == sudo less /etc/profile

vai aparecer essa tela e inserir o comando a seguir na ultima linha comando == !/bin/sh e dar ENTER

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/04340027-fc96-4b0b-bb45-f1cd79f4273a)

e parace que deu certo 

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/2ccdbf7b-91e0-4ff6-9f27-753105e795fc)

BOOM!

![image](https://github.com/EvelynMurasaki/CTFs-Resolucoes/assets/26422836/0e5bc195-ed51-4a69-8e54-c07e5876b4c3)

E finalizado. Esse foi o CAMINHO 1 pelo Jake.

## CAMINHO 02 HOLT



