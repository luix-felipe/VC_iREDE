# Resultados da Atividade 5

As tabelas são geradas por `notebooks/atividade_5.ipynb`, que também apresenta os
resultados com nomes legíveis e interpretações. Os nomes internos dos CSV servem
ao código; as tabelas visuais não exibem caminhos de arquivos de saída.

| Arquivo | Conteúdo |
|---|---|
| `estatisticas_globais.csv` | Média, variância populacional, desvio e entropia das 10 fotos originais; médias RGB auxiliares |
| `faixas_intensidade.csv` | Proporções de pixels escuros, médios e claros de quatro fotos |
| `derivadas.csv` | Comparação de uma original e sua versão de 20% por classe |
| `pontos_interesse.csv` | Quantidades de cantos Shi-Tomasi e blobs LoG |
| `ajuste_blobs.csv` | Contagem de blobs com limiares 0,08, 0,12 e 0,18 |
| `matching.csv` | Keypoints, candidatos e matches aceitos após o teste de razão em três pares |
| `ajuste_matching.csv` | Mesmos descritores e pares, com razões 0,60, 0,75 e 0,90 |
| `robustez.csv` | Controle e borramento: quantidades de keypoints e matches aceitos |
| `glcm.csv` | Quatro propriedades por classe e ângulo, em recortes de 512×512 |
| `lbp.csv` | Dez categorias normalizadas por recorte |
| `sintese.csv` | Comparação crítica dos cinco tipos de descritor |

Os histogramas globais usam 256 níveis fixos. A GLCM usa 16 níveis, distância 1 e
ângulos 0°/90°. O LBP é uniforme, P=8 e R=1, excluindo a borda do histograma.
As imagens locais têm lado máximo 1.000; os patches usam pixels originais orientados.

As figuras e imagens resultantes ficam em `dataset/derivadas/atividade_5/`.
Os originais em `dataset/originais/` e as derivadas da Atividade 1 são somente entradas.
GLCM/LBP descrevem um recorte de cada classe.

A figura de blobs usa limiar 0,18, escolhido após comparar as três sensibilidades.
Os histogramas LBP são exibidos com a mesma escala vertical, ajustada aos dados, e
também em uma tabela percentual por categoria. As médias da GLCM aparecem em sua
própria seção. A análise e a conclusão relacionam esses valores às imagens.

A entrega simplificada não usa homografia nem RANSAC. A tabela de robustez apresenta
somente contagens de pontos e matches; a qualidade das associações é discutida a partir
das figuras. O material aprofundado permanece na aula pessoal e no arquivo histórico.
