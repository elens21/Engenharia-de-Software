# Gerenciamento de Dispositivos
## Gerenciamento de memória
Memória é o lcoal de armazenamento de informações e o seu gerenciamento em um S.O é importante para garantir a eficiência das aplicações que rodam no computador.  
O conceito de hierarquia de memória, pode ser representado da seguinte maneira:  
```mermaid
    graph LR
    A["Uma pequena quantidade de memória cache"]
    B["Uma grande quantidade de memória principal RAM"]
    C["Uma memória secundária com as informações armazenadas em disco"]
```
A hierarquia de memória é controlada pelo **gerenciamento de memória**, responsável por gerenciar quais partes estão em uso e quais não estão, alocando-a quando os processos precisarem, liberando-a após o término dos processos e controlando a troca de processos entre a memória e o disco quando a memória principal não é suficiente para manter todos os processos em execução.
![imagem: hierarquia de memoria](//imagens%20para%20anexar/hierarquia-de-memória.png)
A hierarquia pode ser representada por uma pirâmide. Quanto mais alto as memórias estiverem, mais caras elas serão, ou seja, posuirão alta velocidade de processamento e baixa capacidade de armazenamento. E quanto mais baixa, mais baratas serão, ou seja, possuirão grande capacidade de armazenament e baixa velocidade de processamento.  
O gerenciamento de memória pode ser divido em duas classes:  
- Sistemas que fazem troca de processos e paginação.  
- Sistemas que não fazem troca de processos e paginação.  
### Monoprogramação sem troca de processos ou paginação
Esse mecanismo de gerenciamento é o mais simples, no qual somente um programa é executado por vez e a memória é compartilhada entre o sistema operacional e o programa.  
Ela pode ocorrer em 3 formas:  
![imagem: monoprogramacao](//imagens%20para%20anexar/gerenciamento%20de%20memoria%20-%20monoprogramacao%20Fonte%20Tanenbaum%202003%20p140.png)  
- a: O S.O está utilizando o espaço de endereçamento de RAM(memória principal) 
- b: O S.O está utilizando o espaço de endereçamento em ROM(tipo de memória que permite apenas leitura)  
- c: Os drivers de dispositivos estão em ROM e os programas do usuario e o S.O está em RAM

### Multiprogramação com partições fixas
Esse mecanismo está presenta na maioria dos sistmas operacionais modernos. Ele permite que vários processos executem ao mesmo tempo e quando um processo é bloqueado aguardando uma informação de entrada/saída, outro processo poderá utilizar a CPU.  
Aqui  memória é divida em *n* partições de tamanhos diferentes, podendo ser definida quando o sistema for iniciado. Quando um processo chega para ser executado, ele é inserido em uma fila associdada à menor partição suficiente para armzená-lo.  
A vantagem desse método é que podem existir muitos processos aguardando para serem executados em algumas partições e em outras filas não exista nenhum processo.  
![imagem: multiprogramacao com particoes fixas](//imagens%20para%20anexar/gerenciamento%20de%20memoria%20-%20multiprogracao%20Imagem3-p-500.png)  
Para solucionar o problema de espera na execução de um processo, podemos implementar uma fila única, assim um processo mais próximo do início da fila e que caiba na partição é carregada e executado. (**imagem: Partições fixas com filas únicas de entrada**)
![imagem: Particoes fixas](//imagens%20para%20anexar/gerenciamento%20de%20memoria%20-%20particoes%20fixas%20filas%20unicas%20-%20Imagem4-p-500.png)  
Nas linguagens de programação o gerenciamento da memória é fundamental, pois a tendência das aplicações dos usuários é consumir cada vez mais a memória. Em muitas linguagens não é necessário se preocupar com o gerenciamento, porém é importante que seam conhecidas as restrições e capacidades do gerenciador de memória para uma programação eficaz.  


## Fluxo de gerenciamento de recursos de meória e de processador
O gerenciamento de memória também conhecido como MMU(**Mmemory Management Unit**). Sua função é mapear os endereços lógicos em que estão as instruções nas memórias físicas.  
O acesso ao endereço lógicoque é gerado pelo processo e com isso a **MMU** direcionará o endereço lógico para o mesmo correspondente na memória física.

## SWAPPING
A troca de processos (swapping) é realizado quando não existe memória principal suficiente para executar todos os programas do computador o mesmo tempo.  
Na troca de processos um programa é totalmente carregado em memória e executado por um tempo definido, enquanto os demais programas aguardam, em disco, sua vez de executar.  
O swapping traz totalmente cada processo para a memória, o executa por algum tempo e o retorna para o disco. A figura presenta como se dá o funcionamento da troca de processos na memória principal.  
![imagem: swapping](//imagens%20para%20anexar/swapping%20-%20Imagem1-p-500.png)
Exemplificando o conceito:  
- Um computador possui uma memória de 512MB e tem 4 processos para serem executados com os tamanhos de 481MB, 508MB, 380MB  e 369MB, respectivamente.  
- O gerencimanento de memória seleciona um processo inteiro para ser executado em memória e os demais processos aguardam em disco a sua vez de executar.  
- Se o primeiro processo (com o tamanho de 481MB) for selecionado para ser executado, ele é carregado para a memória e executado por um tempo determinado.  
- Assim que o tempo finalizar, o processo retorna para o disco e outro é selecionado para executar.  
- Importante: para a seleção do processo que será executado são utilizados algoritmos que utilizam de critérios para realizar a escolha.  
O swapping permite um maior compartilhamento da memória principal e utilização dos recuros do sistema..  
Porém quando existe pouca memória RAM disonível, o sistema pode ficar dedicado a execução do swapping, deixando de realizar as tarefas mais críticas, se tornando ineficiente.

## Multiprogramação com partições variáveis
A alocação particionada variável consiste em ajustar dinamicamente o tamanho das partições de memória quando os processos chegam para serem executados. Ou seja, cada processo utiliza um espaço necessário para executar, não acontecendo a fragmentação interna.  
A vantagem das partições variáveis é a flexibilidade por não estar preso a um número fixo de partições, melhorando a utilização da memória, porém impactando o gerenciamento das trocas de processos e na alocação e liberação da memória. 
Quando processos precisam consumir mais memória durante o processamento, é necessário alocar memória dinamicamente. Existem dois métodos de gerencimento de memória com alocação dinâmica:  

### Gerenciamento de memória com mapa de bits: 
![imagem: mapa de bits](//imagens%20para%20anexar/multiprogramacao%20com%20particoes%20variaveis%20-%20maa%20de%20bits-p-500.png)  
Nesse método a memória é dividida em unidades de alocação, a qual é associada a um bit no mapa de bits. Se o valor do bit for 1, indica que a unidade está ocupada, e se o bit for 0, ela está livre.  
A imagem **(a)** acima mostra uma parte da memória com 5 segmentos alocados a processos (A,B,C,D e E) e 3 segmentos de memória livre (espaços vazios).
A imagem **(b)** mostra o mapa de bits correspondete a memória.  
Segmento é uma área de memória alocada a um processo ou uma área livre de memória entre dois processos.  
### Gerenciamento de memória com listas encadeadas
![imagem:listas encadeadas](//imagens%20para%20anexar/multiprogramacao%20com%20particoes%20variaveis%20-%20listas%20encadeadas%20-%20Imagem3-p-500.png)
Aqui consiste em manter uma lista encadeada de segmentos alocados e livres na memória.  
A figura **(a)** mostra uma parte da memória cm cinco segmentos alocados a processos (A, B, C, D e E) e 3 segmentos de memória livre (espaços vazios). A figura **(c)** apresenta a lista encadeada e a memória dividida emuunidades de alocação.  
Cada elemento dessa lista especifica um segmento de memória disponível (H) ou de memória alocada ao processo (P), o endereço no qual se inici o segmento e um ponteiro para o próximo elemento  da lista.  
## Algoritmos de troca de processos
Para definir em qual área livre os processos serão executados por meio da lista encadeada são utilizados os algoritmos.   
- Fisrt Fit (O primeiro que couber): É o algoritmo mais simples e que consome menos recurso do sistema. O gerenciador de memória procura ao longo da lista por um segmento livre que seja suficientemente grande para esse processo.  
- Next Fit (O próximo que couber): Este algoritmo é uma variação do Fisrt Fit. A posição em que encontra o segmento de memória disponivel é memorizada não precisando percorrer toda lista quando se quer alocar.  
- Best Fit (Melhor que couber): Percorre toda a lista e escolhe o menor segmento de memória livre suficiente ao processo. Este algoritmo é mais lente uma vez que procura em toda a lista.  
- Worst Fit (Pior que couber): Sempre é escolhido o maior segmento de memória disponivel de maneira que , quando divididoo segmento disponível restante deve ser suficientemente grande para ser útil depois.  
- Quick Fit (Mais rápido que couber): Algoritmo rápido e mantém listas separadas por tamanhos de segmentos de memória mais solicitados disponível.

## Alocação de memória
Há 3 tipos:  
- Alocação contígua simples: Mais voltada pra realidade dos primeiros S.O (mais antigos). Sendo a memória principal divida em 2 grandes áreas: uma para alocar o sistema operacional e outra para alocar as aplicações do usuário.  
Dessa fora o desenvolvimento dessas aplicações de usuário tinha que respeitar os limítes da área de alocação disponível pras aplicações de usuário predeterminadas.  
- Técnica de overlay: Considera que diante de uma aplicação, a divisão de módulos auxiliará na determinação do espaço de memória necessária a executar os módulos de forma independente.
- Divisão da aplicação em módulos
