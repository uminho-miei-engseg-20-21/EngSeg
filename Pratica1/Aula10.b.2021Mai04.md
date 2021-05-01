# Aula TP - 04/Mai/2021

Cada grupo deve colocar a resposta às perguntas dos seguintes exercícios na área do seu grupo no Github até ao final do dia 18/Mai/2021. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.



## Exercícios

### 1\. Vulnerabilidade de inteiros


Grave os ficheiros da diretoria [Aula 10.b](Aula10.b) na sua máquina local.


#### Experiência 1.1

Utilize o programa IntegerCheck.java para verificar os valores máximos e mínimos dos vários inteiros na sua máquina.

+ Quantos bits tem cada um dos inteiros?


#### Experiência 1.2

Teste o programa IntegerError.java e verifique o que ocorre em situação de _integer overflow_.

+ Teste com outros tipos de inteiro: byte, short, long

+ E se precisar de utilizar inteiros maiores?

#### Experiência 1.3

Teste o programa IntegerCheck2.java e insira valores correctos e incorrectos.

+ O que acontece quando lê um long e o atribuí a outro tipo de inteiro?
+ O que acontecia se utilizasse o scan para o tipo correcto em cada um dos casos (nextByte(), nextInt(), ...)?


#### Pergunta P1.1

Analise o programa overflow.c.

1. Qual a vulnerabilidade que existe na função _vulneravel()_ e quais os efeitos da mesma?
2. Complete o _main()_ de modo a demonstrar essa vulnerabilidade.
3. Ao executar dá algum erro? Qual?

#### Pergunta P1.2

Analise o programa underflow.c.

1. Qual a vulnerabilidade que existe na função _vulneravel()_ e quais os efeitos da mesma?
2. Complete o _main()_ de modo a demonstrar essa vulnerabilidade.
3. Ao executar dá algum erro? Qual?
4. Utilize as várias técnicas de programação defensiva introduzidas na aula teórica para mitigar as vulnerabilidades.
   + 4.1 Explique as alterações que fez.

#### Experiência 1.4

Analise o programa erro_sinal.c.

1. Qual a vulnerabilidade que existe na função _vulneravel()_ e quais os efeitos da mesma?
2. Complete o _main()_ de modo a demonstrar essa vulnerabilidade.
3. Ao executar dá algum erro? Qual?

#### Experiência 1.5

Analise o programa y2k38.c.

1. Compile-o e execute-o. Do resultado obtido o que pode dizer sobre a arquitetura onde o mesmo foi copilado? Porquê?
2. Compile-o agora com a opção `-m32` do gcc. Qual o resultado? Porquê?

Na questão 2, no caso de não conseguir compilar tem que instalar a biblioteca _multilib_ do gcc. Na máquina virtual pode fazê-lo através do seguinte comando:
> sudo apt-get install gcc-multilib
