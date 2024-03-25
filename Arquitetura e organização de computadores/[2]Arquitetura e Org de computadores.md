# Arquitetura CISC
(Processo com conjunto de instruções) Possui uma grande quantidade de instruções com múltiplos modos de endereçamento.  
Os processadores com essa tecnologia são capazes de processar centenas de conjuntos complexos de instruções.  
Os projetistas de arquitetura CISC consdieram 3 aspectos básicos:  
- Utilização de microcódigo (quanto menor o códigom menos recurso ele utiliza) 
- Construção de conjuntos com instruções completas e eficientes.  
- Criaçao de instruções de máquinas com complexidade similar aos comendos de linguagens de alto nível  
Nesse modelo, o objetivo era a criação de um conjunto númeroso de funções, na maioria das vezes complexas e com vários operandos, o que aumentava o tempo de execução.  

# Arquitetura RISC
A ideia original era entregar um conjunto mínimo de instruções que poderiam realizar todas as operações essenciais: movimentação de dados, operações para ULA e desvios. Somente instruções explícitas LOAD e STORE tinham permissão para acessar a memória.  
A cada ciclo de clock uma instrução é selecionada e executada. Essa arquitetura contém uma menor quantidade de modos de endereçamento, maior quantidade de registradores e uso de pipelining.  
O **pipeline** é a divisão de uma instrução em muitas partes, para que cada parte seja manipulada por uma parte de hardware dedicada e com isso todas as partes possam ser executadas em paralelo.  
Nessa arquitetura existe uma diminuição da quantidade de instruções disponíveis e o modo de endereçamento em relação a arquitetura CISC.  
As máquinas RISC utilizam os registradores da CPU para armazenamento dos parâmetros e variáveis em chamadas de funções e rotinas.  
Processadores ARM usados em celulares, são um exemplo de uso da arquitetura RISC, outros exemplos são os consoles como Nintendo e Playstation  

# RISC X CIS
Um vez que o tempo para buscar uma instrução não é mais uma preocupação e com memória barata para armazenas uma quantidade grande de instruções, não existe uma vantagem real em instruções CISC.  
Todas as instruções RISC tem tamanho fixo.  
Todas as instruções RISC efetuam operações simples que podem ser iniciadas no pipeline a taxa de uma por ciclo do clock.  
A RISC é mais rápida pois usa registradores e os registradores estão no topo da pirâmide da hierarquia de memória.  

# Portas Lógicas e Funções
Um computador é constituido de elementos eletrônicos, como resistores, capacitores e principalmente transistores. Nesses computadores, os transitores são componentes de determinados circuitos eletrônicos que precisam armazenar os sinais binários e realizar certos tipos de operações com eles. Esses circuitos, chamados de circuitos digitais, são formados por pequenos elementos capazes de manipular grandezas apenas binárias. Os pequenos elementos referidos são conhecidos como portas (gates) lógicas, por permitirem ou não a passagem desses sinais, e os circuitos que contêm as portas lóicas são conhecidos como circuitos lógicos.  


# Arquiteturas Paralelas
Fornece uma estrutura explícita e de alto nivel para o desenvolvimento de soluções utilizando o processamento paralelo atraves da existência de múltiplos processadores que cooperam para poder resolver problemas através de execução concorrente

## SISD - Single Instruction, Single Data
- Um único fluxo de instruções
- Um único fluxo de dados
- Máquinas de Von Neumann  
- UC = Unidade de controle  
- UP = Unidade de processamento  
- MEM = Memória

## SIMD - Single Instruction, Multiple Data
- Um único fluxo de instrução  
- Multiplos fluxos de dados  
    - Execução sincrona da instrução para todos os dados  
- Processadores vetorias  
- GPU
## MISD - Multiple Instruction, Single Data
- Multiplos fluxos de instrução  
- Um unico fluxo de dados - Execução de várias instruções em um único dado
