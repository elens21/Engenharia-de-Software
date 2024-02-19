# Gerenciamento de Dispositivos
## Gerenciamento de memória
A hierarquia de memória é controlada pelo **gerenciamento de memória**, responsável por gerenciar quais partes estão em uso e quais não estão, alocando-a quando os processos precisarem, liberando-a após o término dos processos e controlando a troca de processos entre a memória e o disco quando a memória principal não é suficiente para manter todos os processos em execução.
![imagem: hierarquia de memoria](//imagens%20para%20anexar/hierarquia-de-memória.png)

## Fluxo de gerenciamento de recursos de meória e de processador
O gerenciamento de memória também conhecido como MMU(**Mmemory Management Unit**). Sua função é mapear os endereços lógicos em que estão as instruções nas memórias físicas.  
O acesso ao endereço lógicoque é gerado pelo processo e com isso a **MMU** direcionará o endereço lógico para o mesmo correspondente na memória física.

## Alocação de memória
Há 3 tipos:  
- Alocação contígua simples: Mais voltada pra realidade dos primeiros S.O (mais antigos). Sendo a memória principal divida em 2 grandes áreas: uma para alocar o sistema operacional e outra para alocar as aplicações do usuário.  
Dessa fora o desenvolvimento dessas aplicações de usuário tinha que respeitar os limítes da área de alocação disponível pras aplicações de usuário predeterminadas.  
- Técnica de overlay: Considera que diante de uma aplicação, a divisão de módulos auxiliará na determinação do espaço de memória necessária a executar os módulos de forma independente.
- Divisão da aplicação em módulos

## Gerenciamento de memória
Pode ser dividio em duas classes:
- Sistemas que durante o processamento levam e trazem informações da memória para o disco (troca de processos e paginação)  
- Sistemas que não o fazem. A troca de processos (swapping) carrega todo o programa para a memória principal, o executar por um determinado tempo e depois o mesmo retorna para o disco. A paginação divide a memória em partições para a execução das aplicações.
### Monoprogramação sem troca de processos ou paginação
Esse método de gerenciamento de memória, é o mais simples pois somente um programa é executado por vez, a memória é compartilhada entre o sistema operacional o programa. Temos 3 formas em que pode ocorrer esse tipo: 
- O sistema operacional está utilizando o espaço de um endereçamento em RAM.  
- O sistema operacional está utilizando espaço de endereçamento em ROM somente para a leitura.  
- Os drivers de dispositivos estão em ROM e os programas do usuario e o S.O estão em RAM.