# Atividade 2 — Suavização e detecção de bordas

O notebook `notebooks/atividade_2.ipynb` executa as quatro partes do enunciado usando
`fpga_03.jpg`, `fpga_04.jpg`, `contrabaixo_04.jpg` e `contrabaixo_05.jpg`.
Os originais são corrigidos pela orientação EXIF e processados em resolução integral.

As tabelas são geradas novamente pela execução do notebook:

- `selecao_imagens.csv`: classes, dimensões e recortes de detalhe, em coordenadas `(x0, y0, x1, y1)`.
- `suavizacao.csv`: média e variância populacional para a original e seis filtros (28 linhas).
- `escolha_filtros.csv`: filtro escolhido para cada uma das quatro imagens.
- `bordas_antes.csv` e `bordas_depois.csv`: quantidade de pixels de borda
  para Sobel, Prewitt e três pares de limiares Canny (20 linhas por etapa).
- `comparacao_bordas.csv`: comparação pareada por imagem e método (20 linhas).
- `sintese.csv`: resultados com Gaussiano σ=1 e Canny 80/160 (4 linhas).
- `ambiente.json`: versões efetivamente utilizadas na execução.

As fotografias em cinza, os seis resultados de suavização e as máscaras de bordas ficam
em `dataset/derivadas/atividade_2`, separadas por etapa e classe. As figuras também são
salvas em PNG nessa pasta e incorporadas às saídas do notebook para consulta direta.
Os gradientes assinados são apresentados nas figuras; as máscaras salvas de Sobel e
Prewitt resultam do limiar aplicado à magnitude normalizada.

## Critérios de comparação

Sobel é normalizado por 4; Prewitt, por 3. Ambos usam magnitude ≥20 para contar pixels.
Canny utiliza 40/80, 80/160 e 120/240, `apertureSize=3` e `L2gradient=True`.
Os limiares são mantidos antes e depois do Gaussiano σ=1 (janela 7×7).
Os valores Canny não estão na escala dos gradientes normalizados.

A variância também depende da textura e do contraste, não apenas do ruído.
A continuidade das bordas é analisada visualmente nos recortes e nas vistas gerais.
Contagens não são comparáveis diretamente entre Canny e máscaras de gradiente espessas.
Sem referência limpa ou bordas anotadas, não se calcula precisão de detecção nem
quantidade real de falsos positivos. Não foi acrescentado ruído sintético.

A entrega foi simplificada para manter as medidas pedidas no enunciado: média, variância
e contagem de bordas. Não usa região auxiliar, desvio local, média de gradientes nem
contagem de componentes. Os recortes de detalhe permanecem para permitir comparação visual.

Como não foi identificado ruído significativo nas fotografias, o notebook também contém
um experimento visual controlado sobre um recorte da `fpga_04.jpg`. Ele acrescenta ruído
gaussiano (desvio-padrão 18) e sal e pimenta (5%) com semente fixa, comparando média,
Gaussiano e mediana. Esse experimento não altera as imagens originais, não cria linhas
adicionais nos CSV e não é usado para alegar melhora nas capturas reais.

## Execução

Abra o notebook e execute todas as células. Pode ser iniciado pela raiz ou pela pasta
`notebooks`; no Colab, a preparação localiza ou clona o repositório público.
Requer as mesmas bibliotecas da atividade 1. Não depende de saídas da primeira atividade.
As tabelas exibidas têm cabeçalhos legíveis e não mostram caminhos de arquivos derivados.
