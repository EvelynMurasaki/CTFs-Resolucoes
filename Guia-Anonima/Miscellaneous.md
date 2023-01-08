# Desafios realizados em Miscellaneous.

##01

Neste desafio foi fornecido usuario e senha e a sua unica pista foi "hidden" que significa escondido.

![image](https://user-images.githubusercontent.com/26422836/211172702-e296bea7-8c60-40a4-b1e1-4f389d788e3c.png)

Após realizar o login, analisar o ambiente e verificar se tem alguma pegadinha

![image](https://user-images.githubusercontent.com/26422836/211172748-305813f7-d9b7-4e02-84bb-60050d1164d1.png)

Aparentemente é um servidor comum, então porque não verificar quais serviços ele esta executando?!

comando: ps aux

e para a supresa a flag apareceu.

![image](https://user-images.githubusercontent.com/26422836/211172780-e1ed07ad-ceb8-42dc-bee4-ec1c88666e06.png)


##02
Outro desafio interesasnte foi esse do MD5, como o proprio nome diz "bad md5". ou seja tem algo errado com essa hash, e o que será vamos descobrir.

![image](https://user-images.githubusercontent.com/26422836/211174567-265f9367-891d-4977-9939-3466cc07fc96.png)

no primeiro momento eu pensei que seria uma hash de outro formado e depois que chegaria no MD5, mas estava enganada. Então chegou o ponto de querer entender como funciona uma MD5 e o seu padrão

Primeiro criei uma hash em md5 e depois fui realizando uma comparação da minha hash com a hash do desafio, de cara notamos que ela esta com caracteres maiores.

![U![image](https://user-images.githubusercontent.com/26422836/211174772-953b5a4c-0a09-4596-983d-dc490f7a4ec3.png)

Depois de comparar eu fui apagando as letras que achei fora do padrão.

![image](https://user-images.githubusercontent.com/26422836/211174779-12df880c-4f53-4e1a-9449-6a9e1866f2b3.png)

Ate que cheguei em uma aparentemente valida 

![image](https://user-images.githubusercontent.com/26422836/211174807-a2d72fa8-9bab-42da-95d5-c0e9ea533d5a.png)

Feito isso, consegui encontrar a flag GA{m3rryxm4s}

##03

##04

##05
