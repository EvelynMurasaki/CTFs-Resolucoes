
# Desafio realizado em Stego


##01

Um dos primeiros desafios do CTF foi uma imagem no formato JPG.

![image](https://user-images.githubusercontent.com/26422836/210899819-1e6cbf34-cd9b-4ed0-9b19-312b7e605f07.png)

conteudo da imagem

![image](https://user-images.githubusercontent.com/26422836/210899837-276f903f-25a1-4889-9497-03b9555150bd.png)

Nesse desafio foi baixar uma imagem e utilizar a ferramenta exiftool.

comando usado: exiftool -v santa.jpg

![image](https://user-images.githubusercontent.com/26422836/210900596-a36f052e-da57-4263-beab-2a85713795e2.png)


##02

Esse desafio a ideia também é analisar a imagem e conseguir a flag.

![image](https://user-images.githubusercontent.com/26422836/210900807-a74d37fc-5e42-4aed-8dd0-fa3b6e880a9a.png)

conteudo da imagem:

![image](https://user-images.githubusercontent.com/26422836/210903620-25314657-e4c8-4992-ba55-037055f245e7.png)


Para resolver esse desafio foi necessario utilizar a ferramenta zsteg e coletar a flag.

zsteg -a festa.png

![image](https://user-images.githubusercontent.com/26422836/210903364-65c25314-66d9-4c53-9b04-eef709df3535.png)

Flag encontrada:

![image](https://user-images.githubusercontent.com/26422836/210903420-a1cc4f81-fcd2-4326-bfdd-3b0b11562180.png)


##03

Esse desafio foi disponibilizado um Gif para ser analisado para capturar a flag.

![image](https://user-images.githubusercontent.com/26422836/210900824-b9be3e85-6c6f-4870-9676-cff59fb2a326.png)

Para realizar esse desafio eu precisei utilizar a ferramenta stegsolve.

comando: java -jar stegsolve.jar

![image](https://user-images.githubusercontent.com/26422836/210905801-5e4a6a81-3cf5-48c9-9578-529ae23d1468.png)

Gif sabemos que é um conjunto de varias imagens, então para resolver separei todos frames com a ferramenta e depois realizei a analise de cada imagem para verificar se mostrava a flag.

Modo de uso: 

File >> Open >> arquivo.gif

![image](https://user-images.githubusercontent.com/26422836/210906078-fdbec264-e6a2-42eb-abc6-2f7a550122c3.png)

Analyse >> Frame Browser

![image](https://user-images.githubusercontent.com/26422836/210906198-cfcba4b1-07bb-4e4a-b560-42149e8c4b3e.png)

Note que agora tem 117 imagens, e com isso passei pagina por pagina até encontrar a flag.

![image](https://user-images.githubusercontent.com/26422836/210906308-fb4de318-29c4-414e-b491-2f745d29d1fa.png)

Imagem com a flag encontrada na pagina 82.

![image](https://user-images.githubusercontent.com/26422836/210906495-e93d5f6d-9d43-427b-9e7c-46355321e338.png)

Flag: GA{8fc678df1d5a5b6288e333c3c3ad213b}

##04

![image](https://user-images.githubusercontent.com/26422836/210900872-2b380afb-3bbf-474d-b182-fb69ad3b1dc9.png)
