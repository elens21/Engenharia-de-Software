# Relatorio: Aula Prática - Sistemas Operacionais
## Introdução
Nessa aula prática, foi aplicado o conhecimento adquirido através das aulas, material de leitura e pesquisar, para que na prática sejam aplicados o conceito de máquina virtual, dados, arquivos e diretórios. Assim como nesse processo também poder se familiarizar com os comandos do Linux.  
### Criando a máquina virtual
Seguindo as orientações do guia da aula, foi criado uma máquina virtual *UNBUNTU* utilizando o software VirtualBox, nesse caso para que pudesse executar o Linux dentro do Windows.  
![Captura de tela do meu computador](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/VirtualBox%20Maquina%20virtual%20criada.JPG)

### Utilizando o terminal para criar diretórios e arquivos ...
Utilizando o comando **mkdir**, criei o diretório chamado *ATIVIDADES-LABORATORIO*.  
```bash
#comandos executados no terminal:
    mkdir ATIVIDADES_LABORATORIO 
```
![Resultado:Criando 1º diretório](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/1%20CRIANDO%20DIRETORIO%20CHAMADO%20ATIVIDADES_LABORATORIO%20.JPG)
  
Dentro deste diretório, crei outro diretório chamado atividade1.  
```bash
#comandos executados no terminal:
    mkdir mkdir ATIVIDADES_LABORATORIO/atividade1
```
![Resultado: Criando 2º diretório](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/2%20CRIANDO%20DIRETORIO%20CHAMADO%20ATIVIDADES.JPG)
  
Agora com o diretório atividade1 aberto abri ele no terminal e continuamos.    
Criei um arquivo chamado *disciplinas_semestre* e inseri nesse arquivo as seguintes informações:  
- Sistemas Operacionais
- Redes de Computadores
- Análise de Algoritmos
- Gestão de projetos
- Cálculo Numérico
- Estudos Dirigidos  
Para isso foi utilizado o comando **cat** para criar e realizar a entrada dos dados no arquivo.
```bash
#comandos executados no terminal:
    cat >> disciplinas_semestre
    - Sistemas Operacionais
    - Redes de Computadores
    - Analise de Algoritmos
    - Gestao de Projetos
    - Calculo Numerico
    - Estudos dirigidos
    # No final utilizei o atalho Ctrl D
```
![Resultado: Criando e inserindo dados em arquivo](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/3%20CRIANDO%20E%20INSERINDO%20DADOS%20NO%20ARQUIVO%20.JPG)
Logo apó terminar de escrever as informações, utilizei o atalho *Ctrl D* para informar pro terminal que terminei de inserir os dados que quero inserir no arquivo e assim terminar o processo de entrada, pra assim esses dados serem concatenados no arquivo *disciplinas_semestre*.  

Em seguida, para exibir o arquivo, utilizei também o comando **cat**.
```bash
#comandos executados no terminal:
    cat disciplinas_semestre
```
![Resultado: Exibindo os dados do arquivo no terminal](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/4%20EXIBINDO%20ARQUIVO.JPG)

E continuando, abri o arquivo:
![Resultado: Arquivo aberto](//imagens%20para%20anexar/imagens%20-%20aula%20pratica/5%20ARQUIVO%20ABERTO.JPG)

## Conclusão
A possibilidade de poder utilizar um sistema Linux em um computador que possui um sistems Windows, é graças a máquina virtual que criamos utilizando um software que tem esse propósito, nesse caso o *VirtualBox*. Assim expandimos o potencial do computador para melhor aproveitar os recursos disponíveis.  
Assim como foi apresentado nas Teleaulas, aqui fica vísivel a diferença do Linux pro Windows na questão das Linhas de comando. Enquanto no Windows a maioria das ações geralmente estão vísiveis pro usuário na interface, fáceis de localizar na tela, no Linux utilizamos linhas de comandos pra executar algumas ações. O que podemos tratar como um ponto forte, já que, embora temos a opção de criar um arquivo, abrir o arquivo com algum programa e inserir dados nele, através de linhas de comando no terminal, logo que crio o arquivo já posso logo em seguida realizar um processo de entrada de dados, de forma extremamente prática.  