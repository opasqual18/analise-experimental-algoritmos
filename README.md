Descrição

Este projeto implementa geração de dados binários, algoritmos de ordenação 𝑂(𝑛2) e algoritmos de busca, com coleta de métricas de desempenho (tempo, comparações e trocas).
Os programas foram desenvolvidos para cumprir os requisitos da disciplina Algoritmos e Estruturas de Dados.

Estrutura do Projeto
    ├── codigo/
    │   ├── gerador_dados.c
    │   ├── ordenacao.c
    │   ├── busca.c
    ├── dados/
    │   ├── pequeno_aleatorio.bin
    │   ├── pequeno_crescente.bin
    │   ├── pequeno_decrescente.bin
    │   ├── medio_aleatorio.bin
    │   ├── medio_crescente.bin
    │   ├── medio_decrescente.bin
    │   ├── grande_aleatorio.bin
    │   ├── grande_crescente.bin
    │   ├── grande_decrescente.bin
    └── relatorio.pdf  (adicionado apenas na entrega final)

Conteúdo dos Arquivos

gerador_dados.c
Gera arquivos binários com vetores inteiros nos tamanhos 1000, 10000 e 100000, nos cenários aleatório, crescente e decrescente.

ordenacao.c
Implementa os algoritmos Selection Sort, Insertion Sort, Bubble Sort e Bubble Sort Otimizado.
Também realiza a leitura dos arquivos binários, executa cada algoritmo e registra:
tempo de execução, comparações e trocas.

busca.c
Implementa busca sequencial e busca binária.
Carrega o vetor a partir dos arquivos binários e mede tempo e comparações para valores existentes e inexistentes.

Compilação

Usando GCC:

    gcc gerador_dados.c -o gerador
    gcc ordenacao.c -o ordenacao
    gcc busca.c -o busca


Ou, se preferir warnings:

    gcc gerador_dados.c -Wall -O2 -o gerador
    gcc ordenacao.c -Wall -O2 -o ordenacao
    gcc busca.c -Wall -O2 -o busca

Como Gerar os Arquivos de Dados

Após compilar:

    ./gerador


Os nove arquivos binários serão criados automaticamente dentro de /dados.

Como Executar os Algoritmos de Ordenação

Rodar o programa passando o nome do arquivo binário:

    ./ordenacao dados/pequeno_aleatorio.bin


O programa imprime no console as métricas medidas para cada algoritmo:

tempo

comparações

trocas

Os valores também podem ser redirecionados para um arquivo CSV se desejar:

    ./ordenacao dados/grande_aleatorio.bin > resultados_ordenacao.csv

Como Executar os Algoritmos de Busca
        
    ./busca dados/grande_aleatorio.bin


O programa realiza:
busca de um valor existente e de um valor inexistente, usando busca sequencial e binária, exibindo tempo e comparações.

Requisitos do Sistema

Código compatível com qualquer ambiente Linux ou WSL com suporte a GCC.
Nenhuma biblioteca externa é necessária.
