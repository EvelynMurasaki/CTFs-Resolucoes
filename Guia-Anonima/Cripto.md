

# Desafios realizados em Cripto.


##01## 

Vamos começar pelo desafio de Gifts, nele foi encontrado uma cifra para decifrar, e se atente no nome, porque ele foi a dica para resolver o problema.

![image](https://user-images.githubusercontent.com/26422836/210684113-aa288f56-a1a4-4fa2-8651-c9105803cac1.png)


Para resolver esse desafio foi preciso lembrar das cifras que temos, chegamos na cifra de Vinegere, note que inicialmente disse que a dica do desafio seria o nome, então usaremos o nome gifts como chave para descobrir a cifra e a flag.

Eu utilizei o site: https://cryptii.com/ para realizar o desafio.

![image](https://user-images.githubusercontent.com/26422836/210681564-42447eda-1857-4739-9f38-a5d978b55662.png)

##02##

O proximo desafio é uma carta decifrada, a unica pista que temos é que a flag esta em MD5, mas infelizmente não tem algo diretamente a MD5 para descobrir como decifrar a carta. 

![image](https://user-images.githubusercontent.com/26422836/210684501-92911ec6-b68a-460a-9a5e-d11ae83f9e6c.png)

Carta

![image](https://user-images.githubusercontent.com/26422836/210684398-930a2d40-b4a5-4fb3-8f2a-eb86923b44d7.png)


Foi necessario realizar outras pesquisas sobre cifras, até que ao notar a primeira linha da carta temos algo semelhante, porem todo bagunçado, e o que seria? o Alfabeto, note a primeira linha tem 26 letras igual o alfabeto, mas será que é isso mesmo?! Vamos realizar os testes.

01 = abcdefghijklmnopqrstuvwxyz

02 = qkgexrnsmpwlfiyjbtodczvahu

Aparentemente as coisas estão batendo, segundo teste, agora diretamente na plataforma de decifrar a carta, novamente eu usei o site Cryptii.

![image](https://user-images.githubusercontent.com/26422836/210683646-e5bd9375-2add-4428-873c-82a9cbd3188d.png)

E olha lá, deu certo, conseguimos agora realizar a leitura da carta e vamos pegar a nossa flag.

Resultado final:
GA{c64c218a8907177bd032de8e9c8365fb}


##03##

Esse desafio foi disponibilizado um codigo em python e uma flag em outra linguagem, o desafio era entender o que se passava no codigo.

![image](https://user-images.githubusercontent.com/26422836/210685735-e7016174-2a1d-4532-a6de-a7dd263c9e61.png)

Conteudo do codigo em cripto.py

![image](https://user-images.githubusercontent.com/26422836/210686535-caa6465c-5c87-4b62-88ed-34250e890f6b.png)


Como o codigo funcionava, voce escrevi uma palavra ou mensagem e ele retornava em outra ''lingua'' ou formato de texto, não qual seria o nome correto. 

exemplo

![image](https://user-images.githubusercontent.com/26422836/210685953-455d52ca-b2cc-4a7c-a872-4d07cdde51e6.png)

Então, a minha ideia foi, se ao escrever uma mensagem ele retorna simbolos, porque não realizar o contrario?! Colocar os simbolos e inverter a situação toda, mas note que foi uma questão matematica tudo isso.

Linha sem alteração: c += chr(ord(i) + (ord(k[4]) + 2022 % 135))

Linha com alteração: c += chr(ord(i) - (ord(k[4]) + 2022 % 135))

Trocou o + por -

E vamos realizar os testes.

![image](https://user-images.githubusercontent.com/26422836/210686299-fe309d2d-7ab8-4058-9799-1b9f6bd15b2d.png)

Flag: ĬĦŠŇĝŇěĘĘĕĖņėĕėĞęĕĘņęňęŋĞĞĘĜęĕĖĞŇėŇŢ

![image](https://user-images.githubusercontent.com/26422836/210686378-0867c46d-2ae4-4217-bdb5-95ca9e09a36b.png)

Pronto.



##04##

##05##
