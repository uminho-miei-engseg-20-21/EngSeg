# Aula TP - 02/Mar/2021

Cada grupo deve colocar a resposta às **perguntas** (note que as respostas é apenas às perguntas e não às experiências) dos seguintes exercícios na área do seu grupo no Github até ao final do dia 16/Mar/21. Por cada dia de atraso será descontado 0,15 valores à nota desse trabalho.

Note que os exercícios devem ser efetuados numa máquina Linux.

## Exercícios

### 1\. Números aleatórios/pseudoaleatórios

#### Experiência 1.1

Execute o seguinte comando, que gera 1024 bytes pseudoaleatórios: `openssl rand -base64 1024`


#### Pergunta P1.1

Teste os seguintes comandos, que vão obter 1024 bytes pseudoaleatórios do sistema e os apresentam em base64:

- `head -c 32 /dev/random | openssl enc -base64`
- `head -c 64 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/urandom | openssl enc -base64`

Que conclusões pode tirar? Em que se baseia para essas conclusões ?

> Nota: Após algumas questões levantadas pelos alunos, pelo facto do `head -c 1024 /dev/random | openssl enc -base64` não bloquear até existir entropia suficiente, estive a rever este assunto, e:
>
> - Desde 2020, Linux kernel version 5.6 e superior, o /dev/random só bloqueia quando (ou enquanto) o CPRNG (_cryptographic pseudorandom number generator_) não foi inicializado. Após ter sido inicializado, o [/dev/random e /dev/urandom têm o mesmo comportamento](https://www.phoronix.com/scan.php?page=news_item&px=Linux-5.6-Random-Rework).
> - Discussão sobre a remoção do bloqueio ao /dev/random pode ser lida [aqui](https://lwn.net/Articles/808575/).
> - Para quem quiser testar o funcionamento pré-kernel 5.6, pode utilizar [esta máquina virtual](https://meocloud.pt/link/f188f15b-7145-4e11-b59e-6a64f61084a6/CSI.EngSeg.ova/), que tem definido os seguintes utilizador / password: 
>   + user / user
>   + root / root
>

#### Pergunta P1.2

O haveged - <http://www.issihosts.com/haveged/index.html> - é um daemon de entropia adaptado do algoritmo HAVEGE (_Hardware Volatile Entropy Gathering and Expansion_) - <http://www.irisa.fr/caps/projects/hipsor/> -.

Instale a package haveged na sua máquina com o seguinte comando: `sudo apt-get install haveged` (ou comando similar de instalação do seu _flavor_ Linux).

Teste novamente os seguintes comandos, que vão obter 1024 bytes pseudoaleatórios do sistema e os apresentam em base64:

- `head -c 1024 /dev/random | openssl enc -base64`
- `head -c 1024 /dev/urandom | openssl enc -base64`

Que conclusões pode tirar? Em que se baseia para essas conclusões ?

#### Experiência 1.2

O exemplo utilizando o *java.security.SecureRandom* visto na aula, encontra-se na diretoria das aulas (Aula2/PseudoAleatorio), no ficheiro *RandomBytes.java*.

Analise, compile e execute este exemplo.

Nota: Se tiver problemas com a versão do java ou javac execute os seguintes comandos:

- `sudo update-alternatives --config java`
- `sudo update-alternatives --config javac`

e escolha a versão 9/Oracle.


#### Experiência 1.3

Na diretoria das aulas (Aula2/PseudoAleatorio) encontra o ficheiro *generateSecret-app.py* baseado no módulo eVotUM.Cripto (https://gitlab.com/eVotUM/Cripto-py) - siga as instruções de instalação na [branch develop](https://gitlab.com/eVotUM/Cripto-py/-/tree/develop) que já é _compliant_ com o Python 3 -. Para instalar o módulo eVotUM.Cripto poderá efetuar o comando `git clone -b develop git@gitlab.com:eVotUM/Cripto-py.git`.

1. Analise e execute esse programa de geração de segredo aleatório e indique o motivo do output apenas conter letras e dígitos (não contendo por exemplo caracteres de pontuação ou outros).
2. O que teria de fazer para não limitar o output a letras e dígitos?


### 2\. Partilha/Divisão de segredo (Secret Sharing/Splitting)

#### Experiência 2.1

O exemplo utilizando o *genSharedSecret.php* visto na aula, encontra-se na diretoria das aulas (Aula2/SecretSharing), no ficheiro com o mesmo nome.

Analise e execute este exemplo. Verifique o que acontece se tentar reconstruir o segredo (*reconstroiSecret.php*) com mais ou menos componentes do que as esperadas.

#### Experiência 2.2

O exemplo utilizando o *shares.pl* visto na aula, encontra-se na diretoria das aulas (Aula2/ShamirSharing), no ficheiro com o mesmo nome.

Analise e execute este exemplo. Verifique o que acontece se tentar reconstruir o segredo (*reconstruct.pl*) com mais ou menos componentes do que as esperadas.

#### Pergunta P2.1

Na diretoria das aulas (Aula2/ShamirSharing) encontra os ficheiros *createSharedSecret-app.py*, *recoverSecretFromComponents-app.py* e *recoverSecretFromAllComponents-app.py* baseado no módulo eVotUM.Cripto (https://gitlab.com/eVotUM/Cripto-py) - siga as instruções de instalação na [branch develop](https://gitlab.com/eVotUM/Cripto-py/-/tree/develop) que já é _compliant_ com o Python 3 -. 

A. Analise e execute esses programas, indicando o que teve que efectuar para dividir o segredo "Agora temos um segredo extremamente confidencial" em 8 partes, com quorom de 5 para reconstruir o segredo.

Note que a utilização deste programa é ``python createSharedSecret-app.py number_of_shares quorum uid private-key.pem`` em que:
+ number_of_shares - partes em que quer dividir o segredo
+ quorum - número de partes necessárias para reconstruir o segredo
+ uid - identificador do segredo (de modo a garantir que quando reconstruir o segredo, está a fornecer as partes do mesmo segredo)
+ private-key.pem - chave privada, já que cada parte do segredo é devolvida num objeto JWT assinado, em base 64

B. Indique também qual a diferença entre *recoverSecretFromComponents-app.py* e *recoverSecretFromAllComponents-app.py*, e em que situações poderá ser necessário utilizar *recoverSecretFromAllComponents-app.py* em vez de *recoverSecretFromComponents-app.py*.


Nota: Relembre-se que a geração do par de chaves pode ser efetuada com o comando ``openssl genrsa -aes128 -out mykey.pem 1024``. O correspondente certificado pode ser gerado com o comando ``openssl req -key mykey.pem -new -x509 -days 365 -out mykey.crt``

### 3\. Authenticated Encryption

**Cenário:**

> A sua empresa quer colocar um serviço no mercado com as seguintes características:
>  + cifragem (com cifra simétrica) de segredos;
>  + decifragem do segredo previamente cifrado;
>  + o cliente pode decifrar o(s) segredo(s) que cifrou durante o tempo em que pagar a anuidade do serviço;
>  + de modo ao cliente saber o que cifrou, pode etiquetar o segredo.

> Para tal, a sua empresa adquiriu um hardware específico de cifra/decifra, em que a chave de cifra é automaticamente mudada todos os dias, sendo identificada por "ano.mes.dia". Esse hardware também efectua HMAC_SHA256 e tem uma API com as seguintes funções:
>  + cifra (segredo_plaintext), devolvendo segredo_cyphertext
>  + decifra (segredo_cyphertext, chave_cifra), devolvendo segredo_plaintext ou erro
>  + hmac (k, str), devolvendo o HMAC_SHA256 da str a autenticar com chave secreta k

#### Experiência 3.1

Baseado no cenário identificado, como sugeriria à sua empresa que cifrasse e decifrasse o(s) segredo(s), de modo a garantir confidencialidade, integridade e autenticidade do segredo e da sua etiqueta, utilizando _Authenticated Encryption_? Inclua, na sua resposta, o algoritmo, que utilizando a API, pediria à área de desenvolvimento para implementar, de modo a cifrar e decifrar o segredo.

### 4\. Algoritmos e tamanhos de chaves

O site https://webgate.ec.europa.eu/tl-browser/ disponibiliza a lista de Entidades com serviços qualificados de confiança, de acordo com o Regulamento EU 910/2014 (eIDAS) - falaremos deste Regulamento noutra aula -.

Entre esses seviços encontra-se o serviço de emissão de certificados digitais qualificados para pessoa física, designado por "QCert for ESig".

#### Pergunta P4.1

Cada grupo indicado abaixo deve identificar os algoritmos e tamanhos de chave utilizados nos certificados das Entidades de Certificação (EC) que emitem certificados digitais qualificados, e verificar se são os mais adequados (e se não forem, propor os que considerar mais adequados):
+ Grupo 1 - Austria, para a EC "PrimeSign GmbH";
+ Grupo 2 - Croácia, para a EC "AKD d.o.o.";
+ Grupo 3 - França, para a EC "Equisign";
+ Grupo 4 - Hungria, para a EC "Microsec Micro Software Engineering & Consulting Private Company Limited by Shares";
+ Grupo 5 - Itália, para a EC "CEDACRI S.p.A. ";
+ Grupo 6 - Lituania, para a EC "State Enterprise Centre of Registers";
+ Grupo 7 - Holanda, para a EC "CIBG";
+ Grupo 8 - Portugal, para a EC "AMA - AGÊNCIA PARA A MODERNIZAÇÃO ADMINISTRATIVA I. P.";
+ Grupo 9 - Eslovénia, para a EC "Rekono d.o.o.";
+ Grupo 10 - Bélgica, para a EC "Kingdom of Belgium - Federal Government";
+ Grupo 11 - Alemanha, para a EC "Bundesnotarkammer";
+ Grupo 12 - Noruega, para a EC "Commfides Norge AS";
+ Grupo 13 - Roménia, para a EC "CENTRUL DE CALCUL SA";
+ Grupo 14 - Espanha, para a EC "Dirección General de la Policía ";
+ Grupo 15 - Bulgária, para a EC "Information Services Plc.";
+ Grupo 16 - República Checa, para a EC "eIdentity a.s.".

Nota 1: Para Entidades de Certificação que já tenham vários certificados de EC, considere apenas o último certificado emitido.

Nota 2: Para obter o tamanho das chaves e algoritmos utilizados, deverá:
1. escolher o certificado da EC,
2. selecionar _Base 64-encoded_,
3. copiar o conteúdo do _Base 64-encoded_ e gravar em ficheiro (por ex., cert.crt),
4. inserir -----BEGIN CERTIFICATE----- no inicio do ficheiro,
5. inserir -----END CERTIFICATE----- no final do ficheiro,
6. executar o seguinte comando ``openssl x509 -in cert.crt -text -noout`` (substitua cert.crt pelo nome que deu ao ficheiro no passo 3.)

Nota 3: Na sua resposta inclua o resultado do comando ``openssl x509 -in cert.crt -text -noout``, referido na nota anterior.


