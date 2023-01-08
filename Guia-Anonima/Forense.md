
# Desafios realizados em Forense.

O primeiro desafio é de uma lista de coisas para o Papai Noel, mas será que essa lista um dos pedidos é uma flag? Vamos ve.

![image](https://user-images.githubusercontent.com/26422836/211176854-1f4667d1-0abe-4df8-9436-159c1d8334d3.png)

Conteudo da lista

![image](https://user-images.githubusercontent.com/26422836/211176873-f5759c8b-8eda-4155-8e60-9ccf32290e95.png)

Não temos a flag ainda, parece que é só um PDF comum, mas será que é um PDF mesmo? Vou verificar.

comando: file lista.pdf

![image](https://user-images.githubusercontent.com/26422836/211176908-e4d48791-4338-405a-b912-165516de2377.png)

Parece que é um PDF, mas esta comprimido, realizei uma pesquisa para entender do que se trata o bzip e cheguei no seguinte comando:

bzip2 -dv lista.pdf 

![image](https://user-images.githubusercontent.com/26422836/211176937-b57efbc1-c08e-40a2-bce4-f92a73812f64.png)

Aparentemente ele gerou outro arquivo chamado lista.pdf.out, irei analisar o conteudo do arquivo

![image](https://user-images.githubusercontent.com/26422836/211176949-4803168f-4049-4353-aabd-cefa6a277858.png)

Olha o que foi encontrado, a flag. Desafio concluido com sucesso.
