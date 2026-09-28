# Resultados da atividade 3

O notebook `notebooks/atividade_3.ipynb` utiliza `fpga_04.jpg` e
`contrabaixo_02.jpg`, uma imagem de cada classe.

Arquivos gerados:

- `selecao_imagens.csv`: classe, formato e resolução das imagens escolhidas;
- `ruidos.csv`: parâmetros, porcentagem alterada e PSNR dos dois ruídos;
- `passa_baixa.csv`: PSNR antes e depois dos Gaussianos 3×3 e 7×7;
- `escolha_filtros.csv`: maior PSNR entre os dois kernels para cada situação;
- `sintese.csv`: resumo das cinco etapas solicitadas;
- `ambiente.json`: versões das bibliotecas usadas na execução.

As imagens derivadas ficam em `dataset/derivadas/atividade_3`. O código usa sementes
fixas, então os ruídos e os valores numéricos são reproduzíveis. O PSNR compara o resultado
com a fotografia anterior à adição do ruído artificial; não representa desempenho de
classificação nem substitui a comparação visual.

A versão simplificada removeu validações internas da DFT, gráficos de transferência,
filtragem passa-alta sobre entradas ruidosas e métricas auxiliares. Esses tópicos continuam
na aula pessoal em `rascunhos/atividade_3_gabarito.ipynb`, que não faz parte da entrega.
