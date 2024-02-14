# O que é sistema operacional?
Sempre vai ser algo intermediário entre o software e o hardware.  
O sistema operacional gerencia o Hardware e o Software, ele faz uma interação entre o usuário e o Hardware, nós não controlamos o Hardware, nós executamos algumas ações, ocorre uma verificação e o sistema operacional assume o controle. Se não existisse o sistema operacional, não conseguiriamos fazer certas ações, como acessar a internet por exemplo.  
Cabe ao sstema operacional servir de interface entre os usuários e os recursos disponpiveis no sistema computacinal.
- Por exemplo, quando queremos imprimir:  
    1- Clico em um botão, através de uma aplicação;  
    2- Essa aplicação vai chamar meu sistema operacional;  
    3- O sistema operacional vai se comunicar com o meu Hardware, nesse caso o Hardware é a impressora, ele vai localizar, ver o status da impressora etc  
- Lembrando que as máquinas só processam informações na linguem binária.
O  sistema operacional funciona através de camadas, então temos a seguinte forma:

    | estrutura |
    |-----------|
    |Aplicações|
    |Utilitários|
    |Sistema Operacional|
    |Linguagem de máquina|
    |Microprogramação|
    |Circuitos eletrônicos|

Resumindo: O usuário interage com as **Aplicações**. Essas aplicações interagem com os **utilitários**, e e esses interagem com o **sistema operacional** e esse transforma o nosso pedido em **linguagem de maquina** (*linguagem binária*)e essa trabalha com a **microprogramção** que vai acionar os **circuitos eletrônicos**  
#### Então, qual as principais funções do sistema operacional?
- Oferecer meios para que um programa seja carregado em memória e executado.  
- Um sistema de arquivos, permitindo criar, ler, escrever e excluir arquivos.  
- Uma interface de acesso aos periféricos.  
- Mecanismos de monitoração de recurso, capazes de identificar os possíveis gargalos no sistema.  
- Meios para armazenar/manter o estado do sistema.

### Kernel
O núcleo do sistema se chama Kernel. Esse é composto por um processador, memória, sistema de arquivos, além de gerenciar os dispositivos de entrada e saída. Ele quem faz o gerenciamento dos recursos do computador. As principais funções desse núcleo são:  
- Tratamento de interrupções  
- Gerenciamento, sincronização, comunicação e escalonamento de proecessos e threads  
- Gerenciamento da memória  
- Gerenciamento dos sistemas de Arquivos  
- Gerenciamento dos dispositivos de E/S  
- Auditoria e segurança do sistema  
Os modos de acesso aos serviços do núcleo podem ser realiados de duas formas,  
- Modo usuário: Programas podem executar ações sem privilégio, como a leitura de um arquivo.  
- Modo Kernel: Nesse, o acesso pode ser realizado de modo usuário E de modo com privilégio tota, como o acesso ao disco.  
Quando um programa é executado o kernel é consultado para saber se o acesso será realizado me modo usuário ou kernel.  


### Classificação dos sistemas operacionais
Os sistemas operacionais podem ser classificados em:
|classificação|
|----------------------------|
|Monoprogramáveis/monotarefa|
|Multiprogramáveis/multitarefas|
|Sistemas com múltiplos processadores|

**Monoprogramáveis:** 
Faziam uma tarefa por vez, enquanto não terminasse uma tarefa, ela não faria outra. Utilizava todos os recursos (processador, memória, periféricos etc) para executar uma única tarefa por vez. Um único usuário pode interagir com o sistema.  
**Multiprogramáveis:** 
É permitido que mais de um usuario o utilize. Várias aplicações dividindo os mesmos recursos da máquina.  
**Múltiplos processadores:** 
Utilizam duas ou ais *UCPs* (Unidade Central de Processamento) que trabalham em conjunto. Ou seja, além da máquina poder executar vários proramas simultaneamente, aora o seu processamento pode ser dividido entre os processadores. Esse tipo de sistema pode ser subdivido em: Fortemente acoplados e Fracamente acoplados.
    - Fortemente acoplados: Há vários processadores compartilhando uma única memória física, e os dispositivos de entrada e saída são gerenciados por um único sistema operacional. Por exemplo o Unix e o Windows. Existe uma memória compartilhada por todos os processadores.  
    - Fracamente acoplados: Possuem 2 ou mais sistemas interconectados em rede, sendo que cad asistema opera de forma independente com seu próprio sistema operacional e gerenciamento de recursos de processamento (UCPs), memória e dispoitivos. Cada sistema tem sua própria memória individual

A internet é um sistema operacional de múltiplos processadores fracamente acoplado conhecido também como *Sistemas distribuídos*.

### Unidade funcionais do sistema computacional e Arquitetura do SO 
**Monolítica:** Módulos executados separadamente mas que compõem um único executável. Aqui o SO é escrito como um conjunto de módulos compilados separadamente e depois agrupados em um arquivo executável.  
**Camadas:** Devido a complexidade do sistema, aqui o SO organiza como uma hierarquia de camadas construídas umas sobre as outras. 
**Máquina Virtual:** Faz o intermédio entre o hardware e o sistema operacional, Oferece todos os serviços do Sistema O. Pode haver várias máquinas virtuais em uma única máquina.
**Microkernel:** Menor e mais simples, Trata serviços por processos que oferecem funções específicas.  
Ele tem modos de tratamento de dados em Hardware, Software e Armazenamento  

**Hardware:** Os dados do processo ficam armazenados nos registradores (status, PC e SP)
**Software:** Há especificação de recursos e suas limitações para que possam ser alocados os processos. Nome, ÍD(identificaçao), Owner, prioridade, data/hora, tempo de processador etc
**Armazenamento:** Refere-se a area de memória que será alocado o processo para que possa ser executado
Eis algumas partes da arquitetura do sistema operacional:  
**Processador:** Gerencia o sistema computacional.  
**Unidade de controle (UC):** Gerencia as atividades dos componentes do computador como gravação de dados e localizar instruções.  
**Unidade lógica e Aritmética (ULA):** Realiza operações lógicas e aritméticas.  
**Registradores:** Armazena dados temporariamente. (memórias caras = memórias pequenas)  
**Controlador de instruções (CI):** Contém o endereço da próxima instrução para o processador executar.  
**Apontador da pilha (AP) ou stack pointer (SP):** Refere-se as instruções que estão no topo da pilha de execução, contém seu endereço na memória.  
**Registrador de instruções (RI):** Armazena a insrução que será decodificada pelo processador.  
**Registrador de status ou program status word (PSW):** Armazena informações sobre os processos em execução.  


**Ciclo de busca e instruções do processador:**
```mermaid
    graph TD
    A[Busca na memória principal o endereço CI e armazena RI] --> B[Atualiza o CI com o indereço da próxima instrução] --> C[Decodifica a instrução do RI] --> D[Busca operando em memória]--> E[Busca instrução decodificada e reinicia o processo]
```

Eis os recursos que o sistema operacional gerencia:
**Memória principal:** Acesso pelo endereo que é registrado pelo MAR (memory address register). Através dele, a unidade de controle, saberá onde alocar os dados e sua disponiilidade.
**Memória cache:** Utilizada pra minimizar a diferença entre a velocidade do processador e da leitura dos dados na memória principal. Ela é pequena, porém muito veloz, pois armazena uma parte do conteúdo da memória principal e é acessada primeiro pelo processador. Quanto menor a cache, mais rápido será oa cesso ao dado. Primeiro o processador busca na memória cache e depois vai buscar na memória principal. É uma memória volátil, ou seja, fica armazenada por pouco tempo.
**Memória secundária:** Nao volátil, ou seja, o que gravou, ficou lá gravado. É uma memória barata.
**Dispositivos de entrada e saída:** Hardwares, viabiliza a comunicação entre o sistema computacional e o ambiente externo.
**Barramentos:** Canais que viabilizam a comunicação, as linhas de comunicação entre condutores processadores, memórias e dispositios.
**Pipelining:** Técnica que permite o processador executar várias tarefas paralelamente em estágios diferentes. Divide ua tarefa em sub-tarefas para execução em sequência. Enquanto uma função está sendo executada, ele já está buscando qual é a próxima, para assim agilizar o processamento de forma geral. 
**Arquitertura RISC e CISC:** Processadores interpretarão os dados e as instruções em uma linguagem de máquina. A RISC tem poucas instruções e são executadas diretamente pelo Hardware. A CISC possui instruções mais complexas que são itnerpretadas por miniprogramas da memória RAM.
**Software**
**Tradutor:** Traduz as instruções pra linguagem da máquina
**Interpredator:** 
**linkador**
**Loader:** Carrega na memória principal o programa a ser executado.

----------------
**Throughput:** Essa taxa refere-se a quantidade de dados que são processados e ao tempo que levou para isso acontecer. É aplicavel tanto em transferências em disco rígido quanto em redes de computadores.

### Características dos sistemas multiprogramáveis
**Interrupção:** Ela não depende de um processo em execução, e sim ocorre em função de um evento externo ao prorama que está em uso. Acontece a qualquer momento. E quando ocorre, os dados são armazenados  
**Exceção:** É diretamente ligada ao prorama, ou seja, é um evento ocorrido em função do processamento do programa.  
**Operações de Entrada e Saída:** O controlado ou interface, reconhece os comandos e solitações advindas dos dispositivos e que precisam se comunicar com o hardware e com o software. Assim o processador não se comunica diretamente com o hardware e com o software, e sim com o controlador ou interface. Temos 2 tipos de controladores: E/S controlada por programa e E/S controlada por interrupção  

**Vetor de interrupção:** Guarda o endereço em que está o conjunto de instruções que foram executadas para tratar o evento.
**Registrador de Status:** Armazena qual foi o tipo de evento ocorrido, pois para ada tipo a sua respectiva rotina de tratamento.

#### Sistemas operacionais embarcados: 
São usados por exemplo para computadores de mão: Celulares, aparelhos de TV, mircro-ondas.
Estes sistemas possuem caracteriscas dos sistemas operacioanais de tempo real, mas possuem limitações de memória e consumo de energia.
Ex: tvOs(Apple), WebOs(LG), Tizen(Samsung)

#### Sistemas operacionais Mobile:
São encontrados em celulares,tablets e MP3 Players. São mais simples e érmitem a comunicação de dados sem fio.
Ainda permitem a utilização de rádio, câmera, gravador de voz entre outros.
Exemplos: Android, Windows Phone, iOS, etc. 

#### Sistemas operacionais na Nuvem:
Utilizam os conceitos com base na computaçao na nuve, (os serviços como banco de dados, redes, são feitoas pela internet).
Todos os dados do usuário e aplicativos ficam na nuvem o acesso é via internet.

#### UNIX:
Sistema portavel, multitarefa  

### Diferenaçs entre Windows e Linux:
#### A lincença: 
Para usar o windows é necessario adquirir a licença da Microsoft que é paga, já no Linux a licença o usuário pode aixar em quantas máquinas quiser.
#### Acesso ao código-fonte:
No windows o código-fonte é restrito apenas a seus desenvolvedores. Já o do Linux é aberto e todos os usuários tem acesso e podem modifica-los.
#### Linha de comando:
Um dos pontos fortes do Linux é a linha de comando que permite uma administralão efetiva do sistema operacional o Windows també possui linha de comando, mas não é tao efetiva, porque quase todas as confiurações são realizadas pela interface gráfica
#### Flexibilidade e riidez:
O Linux permite que o usuário adeque o sistema operacional do jeito que ele desejar em relação ao ambiente gráfico. No Windows as regras são definidas pela Microsoft

# Processos e Threads
## Introdução a processos
O sistema operacional é composto basicamente por um conjunto de rotinas que conhecemos como núcleo do sistema (Kernel). O Kernel realiza o controle e tratamento de interrupções e exceções, criar e eliminar processos e threads.
Para a realização dessas várias tarefas, naturalmente o sistem operacional precisará do auxílio de mecanismos de controle para gerenciar essas operações, uma delas é o **system call**.

- A ideia principal é que um processo constitui uma atividade. 
- O processo tem uma entrada, uma saída e um estado e um programa.
- Um único processador pode ser compartilhado entre varios processos.
- A parte mais importante do computador, o processador, ele pode ter vários processos nele, mas quem determina qual processo vai estar la dentro, por quanto tempo, quando entrar, sair etc, é o sistema operacional que determina, auxiliado pelo algoritmo de   
  
Existem os processos iniciados pelo usuário, por exemplo: Executar um editor de texto, abrir uma página na internet, abrir o aplicativo de música.  
Existe tambem os processos iniciados por outros processos, por exemplo; uma página na internet solicitando a ajuda de outro processo pra fazer o carregamento de seus elementos.   
Então outro exemplo que emgloe os dois casos, no meu naveador eu digitei algo na barra de busca e pesquiser, ou seja isso foi um processo que eu usuario iniciei, porem para me retornar os resultados, o site de pesquisa vai fazer a busca da minha pesquisa em outros sites e tal, esse processo de pesquisa em outros sites, é um processo que foi iniciado por outro processo (a minha ação anterior)

Para cada uma das rotinas que o sistema executará, há um mecanismo de controle de *chamadas de sistema* (*system call*) que pode ser explícito ou implícito.
No explícito, há uma instrução de qual chamada deverá ser executada no próprio programa, através da implementação de uma função que carrega os seus respectivos parâmetros.
No implícito á a inserção de um comando da linguagem de programação.
O system call verifica os parâmetros da solicitação e envia sua respectiva resposta com o estado do processo, por exemplo, se está concluido, se houve algum erro etc.

**shell:** É uma interface de usuário para acessar os serviços de um sistema operacional.  
**CPU:** A CPU é responsável por alternar os programas, executando-os por dezenas ou centenas de milissegundos, para que cada um tenha acesso ao processamento, dando a ilusão ao usuário de paralelismo ou pseudoparalelismo.  
O pseudoparalelismo é a falsa impressão de que todos os programas estão executando ao mesmo tempo, mas na verdade o que acontece é que um processo em execução é suspenso temporariamente para dar lugar ao processamento de outro processo e assim sucessivamente.  
Ou seja a CPU alterna de um processo para outro a cada momento, essa alternância é conhecida como **multiprogramção**.  
Os processos do sistema operacional que administram a comunicação entre os eventos e a sua sincronização ocorrem através do envio de sinais.  
Esses sinais são **bits** que compões o bloco de controle de processos também conhecido como **PCB**.  
Se  processo for eliminado, será acionado o bit correspondente ao evento e ele será excluído apenas quando for entrar em execução.  

## Processo X Programa
A diferença entre processos e programa é essencial pro entendimento de conceitos futuros.  
O processo é uma parte de execução de um programa, enquanto um programa é um grupo de operações ordenadas para atingir um objetivo de programação. O processo tende a ser algo mais curto e o programa mais longo.  
[Ler mais sobre](https://pt.stackoverflow.com/questions/131108/existe-diferença-entre-programa-thread-e-processo)

### Lista de definições: Programa  
Programa é uma sequência de instruções codificadas (escritas) a serem executadas pelo computador;  
É um programa em execução;  
Sequência de instruções sem atividade própria.  
O mesmo programa pode ser excutado várias vezes ao mesmo tempo, e mesmo se tratando do mesmo programa eu preciso ter um processo pra cada execução desse programa;
### Lista de definições: Processo
Processo é um conjunto de dados que vai acompanhar a execução de um programa. 

---
```mermaid
    graph TD
    A[O mesmo programa pode ser executado 
    várias vezes ao mesmo tempo, 
    dessa forma tendo um 
    processo pra cada execução]
    A --- B[Programa] 
    B--> C["Execução [1]"]:::exe1 --> F["Processo da exec1"]:::proces1 --> I
    B--> D["Execução [2]"]:::exe2 --> G["Processo da exec.2"]:::proces2 --> I
    B--> E["Execução [3]"]:::exe3 --> H["Processo da exec.3"]:::proces3 --> I
    I[Assim um programa pode 
    ter vários processos ao mesmo tempo]

    classDef exe1,proces1 stroke: #206802
    classDef exe2,proces2 stroke: #f57f17
    classDef exe3,proces3 stroke: #672b26
```

---
Alguns exemplos para exemplificar a diferença entre eles assim como alguns elementos que o compõe.:  
Imagine:  
- Um confeiteiro - *processador*  
- Uma receita de bolo - *programa*  
- Ingredientes do bolo - *dados*   
Processo é a atividade desempenhada pelo cozinheiro (processador) em ler a receita (thread), buscar os ingredientes (thread), bater o bolo (thread) e assar o bolo (thread).

Mas ai imagine que enquanto o cozinheiro estpa fazendo isso, o filho é mordido por um animal. Vendo isso o cozinheiro marca aonde estava na receita (estado atual do processo é salvo) e procura um livro de pronto-socorro que tenha orientações para ajudar o filho.  
Assim o cozinheiro alterna do processo(Cozimento) para outro, de prioridade mais alta (cuidar do filho), sendo que cada um desses processos tem um programa diferente (receita X livro).  
Os processos em espera sao orgaizados no sistema em listas encadeadas e de acordo com o tipo de evento ocorrido. Quando recebem os recursos necessários, mudam para o estado de pronto.

## PCB (Process Control Block)

## Classificação de processos
Dois tipos: 
- **CPU-bound:** Ocupa mais recursos da unidade central de processamento (UCP), passa mais tempo em execução. Facilmente encontrado em aplicações com maior quantidade de operações de cálculo  
- **I/O-bound:** Passa a maior parte do tempo em estado de espera. Encontrado em aplicações comerciais em que é necessário realizar muitas tarefas de leitura, gravação e processamento.  

## Estado do processo
Nos sitemas operacionais multiprogramáveis os processos não devem receber de forma dedicada todos os recursos da máquina.  
Com isso, or processos são dividos em estados: execução **(running)**, pronto **(ready)**, e espera **(wait)**.  
O processo está em **running** enquanto é processao pela UCP (**Unidade Central de Processamento**), sendo que os processos revezam o tempo de processamento controlado pelo sistema operacional.  
Quando o processo se encontra no estado de **ready**, quer dizer que o processo está aguardando para ser processado.  
Já o estado de **wait** acontece quando o processo aguarda um recurso para continuar o processamento, ou o tratamento de um evento para que possa prosseguir.  
- Os processos em **wait** são organizados no sistema em lista encadeas e de acordo com o tipo de evento ocorrido. Quando recebem os recursos necessários, mudam para o estado de **ready**.
## Criação de processo e finalização de processo

```mermaid
    graph TD
    A{Processos}
    A --> |Criação de processo| D[Inicio do sistema;
    Processo em execução;
    Requisição do usuário;
    Tarefa em lote;]
    A --> |Finalização de processo| E["Saída normal(Voluntária)";
    Saída por erro;
    Erro fatal;
    Solicitação de outro processo;]
```
## Hierarquia de processos
É muito comum que um processo seja criado por outro processo que vai criar outros processos e assim em diante, por isso é essencial que o SO administre uma Hierarquia de processos.  
```mermaid
    graph TD
    A[Processo Pai]
    A --- B[ Processo Filho]
    A --- C[ Processo Filho]
    A --- D[ Processo Filho]
```

## Comunicação entre processos e problemas clássicos de comunicação entre processos
Alguns exemplos vão girar em torno do seguinte exemplo.  
Imagine que você é o TI responsavel por uma rede de clinicas médicas. Temos a tarefa de fazer com que seja localizado o endereço de solicitação de informações online do sistema de gestão da clínica médica e informar a partir disso, os consultórios e clínicas mais próximas do usuário de acordo com o seu plano de saúde, além de oferecer o serviço de discagem direta para a realização do aendamento.
## Comunicação entre Sistema Operacional e usuário
O S.O se comunica com o usuário de três formas: através de *procedimentos prórpios do sistema*, por meio da *interação com os aplicativos* ou, ainda, através das *linguagens de comando*.  
Cada um deles tem o seur espectivo *acesso e armazenamento de dados reservados em memória* e se um arquivo for compartilhado por exemplo, será preciso arantir a veracidade e precisão dessas informações.  
Por isso, o acesso as informações deve estabelecer qual é o tipo de comunicação que está acontecendo e se é em modo usuário ou em modo kernel.  
**Modo usuário:** Apenas instruções chamadas não privilegiadas poderão ser executadas e por isso uma quantidade menor de intruções a executar.  
--> Informações não privilegiadas: São aquelas que não oferecem risco ao sistema, e as privilegiadas são as que podem interferir no funcionamento do kernel.  
**Modo Kernel:** O sistema operacional tem acesso irrestrito às intruções do processador


Então como trabalhar com informações, como no exemplo, dar informações do bairro, ver se tem clinicas, preços, disponibildiade, discagem direta etc. Tudo isso por si só já é muita coisa, mas imagine que estamos falando não só de 1 usuário mas sim de vários ao memso tempo, como fazer a administração disso?
### Sincronização de leitura e gravação de processos
A troca de informações para operações de gravação e leitura entre processos concorrentes, em que há o compartilhamento do buffer, que armazenará temporariamente as informações para que sejam acessadas de forma mais rápida para o processamento.  
A **gravação** desses dados ocorre apenas se o buffer estiver vazio, assim como a **leitura** dos dados só acontece se houver dados para leitura.
--> Buffer: É uma área de armazenamento temporário que armazena dados enquanto eles estão sendo transferidos entre diferentes partes do sistema.  
Para realizar a sincronização entre os processos, são acionados o que chamamos de mecanismos de sincronização. Esses visam garantir a integridade e confiabilidade das ações de sistema.  
O *Comando FORK* tem por função realizar uma chamada do processo que está no buffer para ser executado e, a partir da sua identificação, o associa ao seu subprocesso, ou seja o processo filho. Fork também assume a função de acompanhamento de execução desse processo.  
Assim como FORK cria processos, o comando *JOIN* tem o objetivo e sincronizar os processos criados pelo FORK.

### Tratamento de Erros: Semáforos
Para tratar os erros são propostos alguns algoritmos que reduzem a sua probabilidade de ocorrência.  
- Exclusão condicional: Mecanismo que impede que dois ou mais processos sejam executados compartilhando o mesmo recurso simultaneamente.
- Semáforos: São uma forma de sincronização que permite que apenas um processo ou thread acesse um recurso compartilhado por vez, garantindo assim a prática da exclusão mútua com a inserção de condição de acesso à regiao crítica e execução de projetos. O semáforo é uma variável inteira que realiza duas operações:  
- **DOWN**: Trancamento
- **UP**: Destrancamento  
Fundamentalmente a ideia é utilizar o semáforo para permitir a cooperação entre os processos por meio de **sinais**. Dessa maneira, um processo pode ser forçado a esperar num determinado lugar até que receba um sinal específico.  
- Para receber um sinal, usa-se **DOWN** (Trancamento) 
- Para transmitir um sinal, usa-se **UP**(Destrancamento)  
Quando um processo executa uma operação **DOWN**, o valor do semáforo é definido. O processo pode ser eventualmente bloqueado e inserido na fila de espera do semáforo.  
Numa operação **UP**, o semáforo é incrementado e eventualmente, um processo que aguarda na fila de espera deste semáforo é acordado.  
Semáforos que assumem os valores 0 e 1 são denominados os semáforos binários.

Um semáforo com o valor 0 indica que nenhum sinal de acordar foi salvo e um valor maior que 0 indica que um ou mais sinais de acordar estão pendentes.  
Os semáforos podem ser classificados comp:  
**Binario**: Recebem os valores 0 ou 1.  
**Contadores**: Recebem qualquer valor inteiro positivo, além do 0.  
Ou seja, um semáforo com valor iual a 1 significa que nenhum recurso está utilizando o processo e se tiver com o valor igual a 0 significa que o recurso está em uso. 

Assim o semáforo faz com que não ocorra o erro de não ter nada acontecendo, e nem de ficar em um loop infinito


### Escalonamento e threads
--> Considete que você precis realizar um teste de eficiência do sistema operacional quando o sistema de gestão integrada está em execução, e de forma a identificar o comportamento da gerência de processos e como está acontecendo o escalonamento circular por prioridades. Faça isso em simulado de S.O.  
O escalonamento é a realização da distribuição do acesso aos recursos presentes no sistema entre os processos ativos, de uma maneira onde todos os processos que estejam na fila possam utilizar a CPU.

#### Critérios de escalonamento
Alguns critérios de escalonamento são necessários e determinados de acordo com as caracteristicas do sistema operacional. Dentre os critérios podemos elencar a análise de eficiência e utilização do processador.  
O recomendado é que o nível de capacidade esteja ocupando em média 90% para ser considerado alto, ou seja, com bom potencial de aproveitamento do recurso.  
Outro critério para a definição do escalonamento é o **throughput**. Esse é um indicador que mostra quantos processos foram executados dentro de um intervalo de tempo. Quanto maior o throughput maior será também a quantidade de tarefas realizadas naquele determinado período.  
- Tempo de processador/Tempo de UCP: É o tempo que um processo leva para ser executado e finalizado.  
- Tempo de espera: Que define o tempo em que um processo fica na fila dos processos em estado de pronto.  
- Tempo de turnaround: Tempo total que um processo ocupa, desde sua criação até os eu encerramento.  
- Tempo de resposta: Tempo que leva a partir da criação do processo para que este seja atendido pelo sistema.

### Objetivos do Escalonador
- Dar privilégios para aplicações críticas;
- Balancear o uso da CPU entre os processos;
- Ser justo com todos os processos, pois todos devem poder usar o processador;
- Maximizar a produtividade (throuhput);
- Proporcionar menores tempos de resposta para usuarios interativos.

### Critérios de comportamento de processos
- Orientado a processador: Critério que determina que um processo tende a utilizar todos os recursos do processador que lhe foi atríbuido.  
- Operação de E/S: Utiliza o processador apenas para atender as requisições das operações de entrada e saída de dados, em seguida libera o recurso.  
- Processo em lote: Há a alocação de recursos de processamento sem a interação com o usuário para executar um determinado processo ou grupo de processos.  
- Processo interativo: Nesse critério, o usuário precisa participar com as entradas de dados. Os tempos de resposta do processo precisam ser mais rápidos.  

A avaliaçao de um algoritmo de escalonamento está diretamente relacionada à sua seleção.  
Ele deve ser adequado às necessidades de processamento e funcionalidades que devem ser aliadas ao sistema computacional.  
Desse modo, você precis identificar quais sao as necessidades de processamento do sistema.
- Selecionar os critérios de escalonamento: orientado a processador, em lote, interativo, E/S  
- Saber qual tempo de resposta que a aplicação precisa (througtput)
- Equalizar o processamento para que nao exceda os limites de tempo de execução total e diminui o turnaround e o througtput  
