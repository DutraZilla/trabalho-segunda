# trabalho-segunda # Ordenação e Análise de Desempenho — entrega A2


## Descrição
Implementação de três métodos de ordenação em C: *Insertion Sort, **Merge Sort* e *Quick Sort (Lomuto)*. O programa ordena os dígitos do seu RGM (fornecido como string) e executa benchmarks em vetores aleatórios de tamanhos configuráveis.


## Políticas de contagem de passos
- *Comparações*: incremento em steps_cmp toda vez que um teste if relevante ao algoritmo é efetuado para decidir uma ordenação/partição.
- *Trocas / Movimentações*: incremento em steps_swap sempre que um elemento é movido (atribuição que altera posições relevantes) ou o swap é feito.
- Estas políticas estão implementadas em src/sorts.c com macros COUNT_CMP e COUNT_SWAP.


## Como compilar
1. make
2. Executável: ./ordena <RGM-as-string> (ex.: ./ordena 2170246)


## Saída
O programa imprime CSV na saída padrão com colunas:caso pode ser rgm ou aleatorio. Cada medição é a média de 5 execuções.


## Observações importantes
- Evite compilar com -O3 ao medir passos, pois otimizações agressivas podem eliminar/alterar operações contadas. O Makefile usa -O1.
- Altere os tamanhos em src/main.c (array sizes[]) se quiser mais pontos de medição.


## Discussão (sugestão de conteúdo a incluir no README final de entrega)
- Explicar por que Quick/Merge tendem a O(n log n) e Insertion O(n²).
- Mostrar tabelas/plots (exporte o CSV e gere gráficos externamente).
- Indicar sensibilidade a quase-ordenados (Insertion melhora) e a reversos (Quick pode ter piora sem pivot aleatório).
