# Conceitos-memoria-Ram-memoria-Rom-Swap-e-paginacao-de-memoria.
Conceitos memória Ram, memória Rom, Swap e paginação de memória.

Marcelo Morgenstern					GTI Módulo III - Noturno


Conceitos memória Ram, Rom, Swap e paginação de memória


Memória RAM.

A memória RAM é um tipo de tecnologia que permite o acesso aos arquivos armazenados no computador. Diferentemente da memória do HD, a RAM não armazena conteúdos permanentemente. É responsável, no entanto, pela leitura dos conteúdos quando requeridos. Ou seja, de forma não-sequencial, por isso, a nomenclatura em inglês de Random Access Memory (Memória de Acesso Aleatório).
Como funciona
Assim como a mesa, quanto maior a memória RAM, maior sua capacidade de trabalho. Mas a capacidade da mesa é medida em área. Quanto maior a área da mesa, mais livros cabem e mais rapidamente se faz o trabalho. Já a capacidade da memória RAM, mede-se pelo fluxo de bits suportados nas operações.
Ou seja, para se acessar uma grande quantidade de memória  no HD de uma só vez, como muitos programas atuais exigem, é necessário uma grande quantidade de memória RAM. São estes, portanto, os megabites ou gigabites que aparecem nas configurações.

Fonte: http://www.techtudo.com.br/artigos/noticia/2012/02/o-que-e-memoria-ram-e-qual-sua-funcao.html

Memória ROM.
Aqueles que nunca ouviram falar da ROM certamente conhece um primo próximo desse tipo de memória, o CD-ROM, uma mídia ótica que permite apenas a leitura de dados. Ou seja, você não pode gravar arquivos em um CD-ROM, apenas executar ou visualizar o que já estiver nele.
Basicamente, essa é a função da memória ROM: oferecer dados apenas para leitura. Normalmente, a ROM é utilizada para armazenar firmwares, pequenos softwares que funcionam apenas no hardware para o qual foram desenvolvidos e que controlam as funções mais básicas do dispositivo.

Tipos de ROM.
Mask-ROM.
As primeiras ROMs a serem desenvolvidas são as chamadas Mask-ROM, e são nada mais do que circuitos integrados que guardam o software ou os dados gravados durante a sua criação. Podemos compará-las com os CD-ROMs: o usuário acessa aquilo que comprou e não pode gravar outros dados na mídia ou chip.
PROM.
Com o passar do tempo, foram necessárias memórias similares, mas que possibilitassem a inserção posterior de dados. A primeira dessa nova leva foi a Programmable Read-Only Memory (PROM), que permite que o conteúdo seja modificado por meio de um dispositivo conhecido como programador PROM.
EPROM.
Outro tipo muito usado é o Erasable Programmable Read-Only Memory (EPROM). A grande inovação da EPROM é permitir a regravação de dados. O conteúdo do chip pode ser apagado expondo-o à luz ultravioleta por cerca de 10 minutos. Já o processo de reescrita dos dados requer uma voltagem cada vez maior e, com isso, a número de reprogramações acaba sendo limitado.
EEPROM
Um tipo mais recente é a Electrically Erasable Programmable Read-Only Memory (EEPROM) que, como o próprio nome indica, permite que os dados sejam apagados e gravados com o uso de eletricidade. Assim, é possível atualizar o firmware de uma câmera ou de um MP3 Player de maneira muito mais prática, sem precisar remover o chip ROM de dentro do aparelho.

Fonte: https://www.tecmundo.com.br/memoria/9346-o-que-e-memoria-rom-.htm

Memória virtual (SWAP).
Os arquivos de paginação nada mais são do que um espaço no disco rígido reservado para ajudar a armazenar os dados da memória RAM quando ela está cheia. É uma forma de estender a quantidade de memória para os dados temporários utilizados pelos aplicativos em execução sem que você precise fazer um upgrade de hardware.
Podemos dizer que seja uma técnica computacional usada pelos sistemas operacionais para aumentar quantidade de memória real do computador a fim de rodar os programas e o próprio sistema sem travamentos.
Essa memória virtual que vai auxiliar a memória RAM fica armazenada no seu HD e tem diferenças de sistema para sistema, porém cumpre a mesma função.

Fonte: http://www.diolinux.com.br/2014/09/o-que-e-memoria-swap.html

Paginação de Memória.
A paginação permite que o programa possa ser espalhado por áreas não contíguas de memória. Com isso, o espaço de endereçamento lógico de um processo é dividido em páginas lógicas de tamanho fixo e a memória física é dividida em páginas com tamanho fixo, com tamanho igual ao da página lógica. Nisso, o programa é carregado página a página, cada página lógica ocupa uma página física e as páginas físicas não são necessariamente contíguas. O endereço lógico é inicialmente dividido em duas partes : um número de página lógica (usado como índice no acesso a tabela de páginas, de forma a obter o número da página física correspondente) e um deslocamento dentro da página. Não existe fragmentação externa, porém existe fragmentação interna (Ex: um programa que ocupe 201kb, o tamanho de página é de 4 kb, serão alocadas 51 páginas resultando uma fragmentação interna de 3kb). Além da localização a tabela de páginas armazena também o bit de validade, (1 ou TRUE) se a página está na memória (0 ou FALSE) se a página não está na memória. E a transferência das páginas de processo podem ser transferidas para a memória por demanda, levando apenas o que é necessário para a execução do programa ou por paginação antecipada, onde o sistema tenta prever as páginas que serão necessárias à execução do programa. Abaixo um exemplo de páginas constantemente referenciadas:

Segmentação.
Técnica de gerência de memória onde programas são divididos em segmentos de tamanhos variados cada um com seu próprio espaço de endereçamento. A principal diferença entre a paginação e a segmentação é a alocação da memória de maneira não fixa, a alocação depende da lógica do programa. O mapeamento é feito através das tabelas de mapeamento de segmentos e os endereços são compostos pelo número do segmento e um deslocamento dentro do segmento. Cada entrada na tabela mantém o endereço físico do segmento, o tamanho do segmento, se ele está ou não na memória e sua proteção. Para isso ocorrer sem problemas, o sistema operacional mantém uma tabela com as áreas livres e ocupadas da memória e somente segmentos referenciados são transferidos para a memória principal. Nesse modelo diferentemente da Paginação, ocorre fragmentação externa. Abaixo um exemplo de Segmentação:

Paginação com Segmentação.
Se os segmentos são grandes, não dá para mantê-los na memória em sua totalidade. Gerando a ideia de paginar os segmentos só deixando na memória as páginas realmente necessárias a cada segmento. Um exemplo de SO que usa esse conceito é o MULTICS que foi o primeiro sistema com suporte a segmentos paginados. E como funciona? Simples, cada segmento é dividido fisicamente em páginas e o endereço é formado pelo número do segmento, número da página dentro desse segmento e o deslocamento dentro dessa página. Abaixo um exemplo de funcionamento de Paginação com Segmentação no MULTICS:

Fonte: https://terminaldeinformacao.com/2013/01/28/tudo-sobre-paginacao-e-segmentacao/
