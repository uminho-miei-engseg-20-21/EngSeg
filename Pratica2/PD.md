# Avaliação prática 2 - Projeto de desenvolvimento (PD)









De seguida são apresentados os vários projetos de análise de um tema. O relatório final deverá ser colocado na área do Grupo no github até ao dia 30/03/2021, na subdiretoria "AP2-PA".
A apresentação e discussão do trabalho será posteriormente marcada em data/hora a indicar.

## 1. Projetos de tipo 1 - Potencial de Ataque a tecnologia

O objetivo deste projeto é identificar o potencial de ataque estimado, necessário para efetuar ataque a determinada tecnologia, de acordo com a metodologia de avaliação do [Common Criteria](https://www.commoncriteriaportal.org/cc/) / ISO IEC 15408.

Não necessita de ter conhecimentos sobre o Common Criteria, mas se tiver curiosidade pode ver as seguintes apresentações:

+ <https://www.youtube.com/watch?v=ceg4hyrcHJc> - apresentação sucinta, menos técnica (recomendada);
+ <https://www.youtube.com/watch?v=PSAlyxhaf5c> - apresentação extensa, muito técnica.


O método de trabalho proposto é identificar vários cenários de ataque à tecnologia, baseado em riscos identificados, destacando a(s) vulnerabilidade(s) explorada(s) e a estimativa do potencial de ataque que é necessário para realizar os ataques.

Para estimar o potencial de ataque dos atacantes (i.e., o esforço necessário para criar o ataque), deve utilizar a metodologia identificada no anexo B.4 do documento _[Common Methodology for Information Technology Evaluation, Evaluation Methodology, Version 3.1, Revision 5, CCMB 2017-04-004](https://www.commoncriteriaportal.org/files/ccfiles/CEMV3.1R5.pdf)_ (também disponível [aqui](../Bibliografia/CEMV3.1R5.pdf)).

Esta metodologia determina quatro potenciais de ataque diferentes; Básico, Avançado-Básico, Moderado e Alto.
Para calcular o potencial de ataque necessário para explorar uma vulnerabilidade, os seguintes fatores devem ser levados em consideração:

+ a) Tempo gasto para identificar e concretizar o ataque,
+ b) Conhecimento técnico especializado necessário,
+ c) Conhecimento do _design_ e operação do alvo a atacar,
+ d) Janela de oportunidade,
+ e) Hardware / software ou outro equipamento necessário para a concretização do ataque.

Esses fatores são definidos no anexo B.4 do documento indicado acima, sendo fornecida tabela para calcular o potencial de ataque (tabela 3), assim como para classificar o potencial de ataque para explorar o cenário de ataque (tabela 4).

Notas: 

+ Para ajuda, é fornecido o ficheiro [PA.Potencial_ataque.doc](PA.Potencial_ataque.doc) com tabelas para cálculo e justificação do potencial de ataque (secção I). Não se esqueça de adicionar contextualização da tecnologia a analisar e seus riscos, assim como uma conclusão.
+ Grupos com mais de três elementos, deverão adicionalmente identificar contramedidas relevantes para cada um dos cenários de ataque, conforme secção II do ficheiro [PA.Potencial_ataque.doc](PA.Potencial_ataque.doc).


### 1.1 Tecnologia a determinar potencial de ataque

+ Grupo 1 - Potencial de ataque à tecnologia de OTP (_One Time Password_) por SMS
+ Grupo 5 - Potencial de ataque à tecnologia de assinatura qualificada com Cartão de Cidadão
+ Grupo 8 - Potencial de ataque à tecnologia de assinatura qualificada com Chave Móvel Digital
+ Grupo 10 - Potencial de ataque à tecnologia de identificação de pessoas físicas, através de procedimentos de identificação à distância com recurso a videoconferência
+ Grupo 12 - Potencial de ataque à tecnologia de criação de assinaturas eletrónicas à distância, com gestão por um prestador qualificado de serviços de confiança em nome do signatário
+ Grupo 14 - Potencial de ataque à tecnologia de identificação de pessoas físicas, através de procedimentos de identificação à distância com recurso a sistemas biométricos automáticos de reconhecimento facial


## 2. Projetos de tipo 2 - Sistema Gestão de Segurança de Informação

A [família de standards ISO/IEC 27000](https://en.wikipedia.org/wiki/ISO/IEC_27000-series) (ou ISO27K) é constituída por standards de segurança de informação publicados conjuntamente pela _International Organization for Standardization_ (ISO) e pela _International Electrotechnical Commission_ (IEC). 

Esta família de standards fornece recomendações de melhores práticas para gestão de segurança de informação, no contexto integrado de um Sistema de Gestão de Segurança de Informação (SGSI) - _Information security management system_ (ISMS) -. O seu âmbito é vasto, sendo aplicável a todo o tipo de entidades, independentemente do seu tamanho. 

Caso tenha curiosidade sobre esta família de standards, recomenda-se que veja:

+ <https://www.youtube.com/watch?v=C4xm33_bqFg> (em espanhol);
+ os vários episódios da série da Clearsec, que começam em <https://www.youtube.com/watch?v=0gzjTD1tdOw> (em francês, com legendas em inglês);
+ <https://www.youtube.com/watch?v=ltEEZLOUP90> (em inglês).

A [Comissão Técnica _Electronic Signatures and Infrastructures_ (ESI) do ETSI](https://www.etsi.org/committee/esi) publica standards europeus no âmbito das assinaturas digitais e serviços de confiança relacionados (em especial, no contexto do [Regulamento eIDAS](https://eur-lex.europa.eu/legal-content/PT/TXT/PDF/?uri=CELEX:32014R0910&from=ga) - Regulamento (UE) n.o 910/2014 do Parlamento Europeu e do Conselho
de 23 de julho de 2014
relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no
mercado interno e que revoga a Diretiva 1999/93/CE), para fornecer confiança e segurança às transações eletrónicas.

O objetivo deste projeto é analisar e relacionar os requisitos nos standards ETSI sobre um determinado tema, com as recomendações de melhores práticas  efetuada por um standard da família ISO/IEC 27000.

Notas: 

+ Não se esqueça de adicionar contextualização do(s) tema(s) a analisar, assim como uma conclusão onde reflete sobre a adequação dos requisitos do ETSI face às recomendações do ISO.
+ Grupos com mais de três elementos, deverão adicionalmente identificar (e justificar) qual dos requisitos do ETSI e boas práticas do ISO, deverão ser vistas como requisitos a serem seguidos no âmbito de votações eletrónicas _online_.

### 2.1 Temas a analisar e relacionar

Os temas a analisar e relacionar serão entre o [ETSI EN 319 401 v.2.2.1 - Electronic Signatures and Infrastructures (ESI); General Policy Requirements for Trust Service Providers](https://www.etsi.org/deliver/etsi_en/319400_319499/319401/02.02.01_30/en_319401v020201v.pdf) e o [ISO/IEC 27002:2013 - Information technology — Security
techniques — Code of practice for
information security controls](https://trofisecurity.com/assets/img/ISO-IEC_27002-.pdf). Se o link para o ISO 27002 não esiver ativo, podem encontrar o documento [aqui](ISO27002_2013.pdf).

Temas a analisar por grupo:

+ Grupo 2 - Política de segurança de informação (_Information Security Policy_), Recursos humanos (_Human resources_), Gestão de incidentes (_Incident management_)
+ Grupo 6 - Controlo de acessos (_Access control_)
+ Grupo 9 - Segurança ambiental e física (_Physical and environmental security_), Controlos criptográficos (_Cryptographic controls_) 
+ Grupo 11 - Segurança de operações (_Operation security_) - para grupo com 5 elementos, se existir
+ Grupo 13 - Gestão de ativos (_Asset Management_), Gestão de continuidade de negócio (_Business continuity management_) 


## 3. Projetos de tipo 3 - Novo Cartão de Identidade europeu

O [Regulamento (UE) 2019/1157 do Parlamento Europeu e do Conselho de 20 de junho de 2019 que visa reforçar a segurança dos bilhetes de identidade dos cidadãos da União e dos títulos de residência emitidos aos cidadãos da União e seus familiares que exercem o direito à livre circulação](https://eur-lex.europa.eu/eli/reg/2019/1157/oj):

+ É aplicável a partir de 2 de agosto de 2021;
+ Identifica as  normas de segurança aplicáveis aos bilhetes de identidade de cidadão nacional emitidos pelos Estados-Membros e aos títulos de residência emitidos pelos Estados-Membros aos cidadãos da União e seus familiares que exercem o direito à livre circulação na União.

O objetivo deste projeto é analisar o regulamento indicado assim como os documentos técnicos conexos, e elaborar um guia técnico (sem o jargão legal) com as características a que o novo cartão de identidade europeu tem que obedecer.

Notas: 

+ Grupos com mais de 3 elementos deverão identificar as diferenças com o atual Cartão de Cidadão português, devendo para tal consultar (entre outros) a seguinte legislação:
  + [Lei n.o 7/2007 de 5 de Fevereiro](https://dre.pt/application/conteudo/518073) - Cria o cartão de cidadão e rege a sua emissão e utilização.
  + [Lei n.º 91/2015 de 12 de agosto](https://dre.pt/application/conteudo/69992903) - Primeira alteração à Lei n.º 7/2007, de 5 de fevereiro, que cria o cartão de cidadão e rege a sua emissão e utilização.
  + [Lei n.º 32/2017 de 1 de junho](https://dre.pt/application/conteudo/107114304) - Segunda alteração à Lei n.º 7/2007, de 5 de fevereiro, que cria o
cartão de cidadão e rege a sua emissão e utilização, primeira
alteração à Lei n.º 37/2014, de 26 de junho, que estabelece um
sistema alternativo e voluntário de autenticação dos cidadãos
nos portais e sítios na Internet da Administração Pública denominado Chave Móvel Digital, e sétima alteração ao Decreto-
-Lei n.º 83/2000, de 11 de maio, que aprova o regime legal da
concessão e emissão de passaportes.
  + [Portaria n.º 285/2017 de 28 de setembro](https://dre.pt/application/conteudo/108228007) - Relativo à regulamentação das formas de entrega do Cartão de Cidadão e dos respetivos códigos
  + [Portaria n.º 286/2017 de 28 de setembro](https://dre.pt/application/conteudo/108228008) - Relativo aos requisitos técnicos e de segurança a observar na captação da imagem facial e das impressões digitais do titular do pedido e ainda das medidas concretas de inclusão de cidadãos com necessidades especiais na sociedade da informação.
  + [Portaria n.º 287/2017 de 28 de setembro](https://dre.pt/application/conteudo/108228009 ) - Relativo aos mecanismos técnicos de acesso e leitura de dados constantes do circuito integrado; o seu prazo de validade; as circunstâncias em que o Portal do Cidadão  pode receber os pedidos de renovação do Cartão de Cidadão; as condições do seu cancelamento pela via telefónica e eletrónica; a fixação do montante devido pelo IRN à AMA, pela sua função de supervisão do Cartão de Cidadão e dos serviços que lhe estão associados, bem como as regras relativas à conservação do ficheiro com o código pessoal para o seu desbloqueio.
  + [Portaria n.º 190-B/2019](https://dre.pt/application/conteudo/122657688) – Primeira alteração à Portaria n.º 287/2017, de 28 de setembro.

### 3.1 Tema a analisar 


Tema a analisar por grupo:

+ Grupo 3 

## 4. Projetos de tipo 4 - Sistema de identificação eletrónica

O [Regulamento eIDAS](https://eur-lex.europa.eu/legal-content/PT/TXT/PDF/?uri=CELEX:32014R0910&from=ga) (Regulamento (UE) n.o 910/2014 do Parlamento Europeu e do Conselho
de 23 de julho de 2014
relativo à identificação eletrónica e aos serviços de confiança para as transações eletrónicas no
mercado interno e que revoga a Diretiva 1999/93/CE), no seu Capítulo II (Identificação Eletrónica), define os critérios de elegibilidade para notificação dos sistemas de identificação eletrónica, assim como os níveis de garantia dos mesmos ("reduzido", "substancial" e "elevado"). Nesse âmbito, Portugal já tem dois sistemas de identificação eletrónica aprovados, pela [_Cooperation Network_](https://ec.europa.eu/cefdigital/wiki/display/EIDCOMMUNITY/Cooperation+Network+Resources), com nível de garantia "elevado":

+ Cartão de Cidadão, [publicado a 28/02/2019](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX:52019XC0228(01));
+ Chave Móvel Digital, [publicado a 08/04/2020](https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=OJ:JOC_2020_116_R_0005).

A [ENISA](https://www.enisa.europa.eu/) definiu um modelo de maturidade ("_A Maturity Model Framework for eID Schemes_") em que define 5 níveis para avaliar a maturidade do sistema de identificação eletrónica, nas componentes de "_Enrolment_", "_Electronic identification means management and authentication_" e "_Providers management and organisation_".

O objetivo deste projeto é analisar o modelo de maturidade da ENISA e avaliar em que nível de maturidade é que se encontra cada um dos sistemas de identificação portugueses aprovados, assim como identificar quais as lacunas existentes para poder estar de acordo com o nível máximo (nível 5).


### 4.1 Tema a analisar 


Tema a analisar por grupo:

+ Grupo 4  - Cartão de Cidadão
+ Grupo 7 - Chave Móvel Digital


Notas: 

+ Grupos com mais de 3 elementos deverão identificar e propôr as ações necessárias para que to sistema de identificação eletrónico possa estar de acordo com o nível máximo.

