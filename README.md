# Lista de Registros de Tamanho Fixo - TP1 (ECOi2206)

## Sobre o Projeto
Este repositório contém o código-fonte desenvolvido para o Trabalho Prático 1 da disciplina ECOi2206 da UNIFEI - Campus Itabira. O objetivo central do projeto é implementar uma lista de registros de tamanho fixo em C/C++. 

A estrutura gerencia manualmente a alocação e o encadeamento de posições vazias e ocupadas através de variáveis de controle, simulando o comportamento de estruturas mais complexas de armazenamento e gerenciamento de memória.

## Funcionalidades Implementadas
O programa é executado através de um menu interativo que oferece as seguintes operações:

* **Criação da Lista:** Inicializa o sistema solicitando o número de registros `n` e criando a estrutura base com cabeçalho
* **Inserção Padrão:** Insere o registro utilizando o primeiro espaço vazio disponível e o posiciona no final lógico da lista.
* **Inserção Ordenada:** Insere o registro mantendo a lista logicamente ordenada através da sua chave. Esta operação manipula apenas os ponteiros lógicos `FIRST`, `LAST`, `NEXT` e `PREV`, pois os registros não podem ser deslocados fisicamente na memória após alocados 16].
* **Remoção:** Remove registros buscando através de sua chave e libera a posição no encadeamento.
* **Pesquisa:** Busca e retorna registros através de sua chave.
* **Impressão (Percuso Lógico):** Imprime as informações do cabeçalho e os registros navegando partindo do `FIRST` e seguindo sequencialmente os ponteiros `NEXT` até atingir o `LAST`.
* **Impressão da Estrutura:** Exibe a organização física atual do vetor e cabeçalho, permitindo debugar o estado interno da lista.

## Restrições e Lógica Arquitetural
Para atender aos requisitos estritos da disciplina:
* O arquivo base `LR.cpp` foi utilizado como referência. Os cabeçalhos de suas funções e a função `main` original não foram alterados6].
* As navegações de busca de espaços livres e de próximos elementos são feitas **estritamente** através do encadeamento (`quant`, `first`, `last`, `free`, `next` e `prev`). É terminantemente proibido realizar varreduras lineares (ex: loops iterando por todo o vetor do índice 0 ao fim) para procurar posições para inserção; o local correto é sempre apontado pela variável `free`.
