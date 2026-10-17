# Resultados da atividade 4

O notebook `notebooks/atividade_4.ipynb` segmenta a imagem pública `coins.png`, aplica
abertura e fechamento, preenche as silhuetas, identifica componentes e extrai três
características de cada objeto.

Arquivos gerados:

- `morfologia.csv`: área total e componentes brutos em cada etapa;
- `caracteristicas.csv`: área, perímetro e centroide dos 24 objetos.

As máscaras e figuras ficam em `dataset/derivadas/atividade_4`. A imagem original e sua
procedência ficam em `atividade_4/`. Os resultados também aparecem diretamente nas saídas
do notebook.

A contagem final corresponde visualmente às 24 moedas, mas isso não garante contornos
perfeitos. As medidas são em pixels e dependem da máscara produzida pelo pipeline.
