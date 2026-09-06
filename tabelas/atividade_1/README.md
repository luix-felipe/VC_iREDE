# Tabelas da Atividade 1

- `metadata.csv`, na raiz do projeto, registra as condições de aquisição das 10 imagens originais.
- `resolucao.csv` registra dimensões, tamanho e impacto das versões original, 50% e 20%.
- `espacos_cor.csv` registra a interpretação das representações RGB, HSV e escala de cinza.
- `quantizacao.csv` registra os testes com 256, 64, 32 e 2 níveis de cinza.
- `formatos.csv` compara JPEG com compressão e PNG sem perdas.
- `selecao_dataset.csv` documenta a origem e o motivo de escolha de cada imagem do conjunto final.

As classes ativas são `fpga` e `contrabaixo`. `fpga_01.jpg` e `contrabaixo_01.jpg` foram escolhidas como representantes dos experimentos da Atividade 1.

O `metadata.csv` já contém os dados extraídos dos arquivos: dispositivo, data e hora, formato, dimensões, tamanho, ISO, exposição, abertura, distância focal equivalente, zoom, flash e métricas computacionais de brilho, contraste e nitidez. A condição visual, o ângulo e o cenário também foram registrados a partir da inspeção das fotos.

As condições de aquisição foram confirmadas pelo autor: aproximadamente 40 cm para o contrabaixo e 20 cm para a FPGA, usando luz natural do sol vinda da janela do quarto. As variações de iluminação foram produzidas com a cortina e com ajustes de exposição da câmera.

As métricas `brilho_medio`, `contraste_dp` e `nitidez_laplaciana` são medições computacionais auxiliares, não avaliações absolutas de qualidade.

Os campos de resultados experimentais foram preenchidos após a execução do notebook com as medições automáticas e as observações obtidas na inspeção das imagens derivadas.
