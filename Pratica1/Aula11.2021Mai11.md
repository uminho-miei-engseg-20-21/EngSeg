# Aula TP - 11/05/2021

Cada grupo deve colocar a resposta às perguntas dos seguintes exercícios na área do seu grupo no Github até ao final do dia 25/Mai/2021. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

**Nota:**

Grave os ficheiros na diretoria [Aula 11](Aula11) para a sua máquina local.



## Exercícios


### 1\. Validação de Input

#### Experiência 1.1

Analise os ficheiros InputValidation.cpp e InputValidation.java.

1. Explique os dois problemas: (i) utilização do cin/Scanner para leitura, (ii) acesso ao array

2. O que alterava?

#### Experiência 1.2

Analise o ficheiro WhileEx.java.

1. Qual o(s) problema(s) no input do  programa?

2. Altere o programa de modo a validar todo o input e recuperar apropriadamente dos erros.

#### Experiência 1.3

Analise o ficheiro Input.cpp.

1. Qual o(s) problema(s) no input do programa ?

2. Altere o programa de modo a validar todo o input e recuperar apropriadamente dos erros.


#### Experiência 1.4

Analise o ficheiro Input.java.

1. Qual o(s) problema(s) no input do programa ?

2. Altere o programa de modo a validar todo o input e recuperar apropriadamente dos erros.



#### Pergunta 1.1

Analise o programa filetype.c que imprime no ecran o tipo de ficheiro passado como argumento.

1. Existem pelo menos dois tipos de vulnerabilidades estudadas na aula teórica de "Validação de Input" que podem ser exploradas. Identifique-as.

2. Forneça o código/passos/linha de comando que permitem explorar cada uma das vulnerabilidades identificadas na linha anterior.

3. O que aconteceria se o seu programa tivesse permissões _setuid root_?


#### Experiência 1.5

Analise o programa readfile.c que imprime no ecran o conteúdo do ficheiro passado como argumento, a que acrescenta o sufixo ".txt" de modo a garantir que só deixa ler ficheiros em texto.

1. Existe pelo menos uma vulnerabilidade estudada na aula teórica de "Validação de Input" (em conjunto com outra que já estudou) que permite que o programa imprima ficheiros que não terminam em ".txt". Explique.
2. Indique a linha de comando necessária para aceder ao ficheiro _/etc/passwd_.


#### Experiência 1.6

Analise o ficheiro string_formato.c com o exemplo de vulnerabilidade de string de formato dado na aula, e o ficheiro string_formato2.c já sem essa vulnerabilidade.

1. Faça algumas experiências com vários valores de input tanto com o programa com vulnerabilidades como sem vulnerabilidades e tire as suas conclusões.


#### Experiência 1.7

Teste a sua habilidade de identificar problemas de segurança durante a revisão de código. Para tal, complete a _OWASP Security Code Review 101_ em <https://owasp.org/SecureCodingDojo/codereview101/>.

O _OWASP Security Code Review 101_ é parte integrante do [_OWASP Secure Coding Dojo_](https://owasp.org/www-project-secure-coding-dojo/).


#### Experiência 1.8

Uma estratégia importante de segurança é a "_defense in depth_". Explique o que significa. De que modo é que a "_defense in depth_" está relacionada com a validação de input?


#### Pergunta 1.2

Desenvolva um programa (na linguagem em que tiver mais experiência) que pede:

+ valor a pagar,
+ data de nascimento,
+ nome,
+ número de identificação fiscal (NIF),
+ número de identificação de cidadão (NIC),
+ numero de cartão de crédito, validade e CVC/CVV.

Valide esse input de acordo com as regras de validação "responsável", apresentadas na aula teórica.

