# Atividade 5 — Entrega e estudo

O arquivo principal de entrega é `notebooks/atividade_5.ipynb`, com código, figuras,
tabelas, interpretação e conclusão executados. O enunciado utiliza as 10 fotografias
do dataset próprio, sem necessidade de novas imagens nesta pasta.

A revisão segue o padrão de apresentação da Atividade 4: objetivo e escolha de cada
etapa, saídas visíveis, comparação quantitativa, interpretação e limitações. Inclui
testes controlados de limiar LoG e razão do matching, além de uma seção própria de
análise dos resultados. Os comentários foram encurtados para manter o foco no enunciado.
Homografia, RANSAC e métricas geométricas adicionais ficam somente nos estudos pessoais.

## Arquivos necessários

- `dataset/originais/contrabaixo/`: cinco fotografias JPEG.
- `dataset/originais/fpga/`: cinco fotografias JPEG.
- `dataset/derivadas/resolucao/contrabaixo/contrabaixo_01_20.png`.
- `dataset/derivadas/resolucao/fpga/fpga_01_20.png`.
- `requirements.txt`: dependências, incluindo scikit-image.

Preserve os caminhos relativos ao enviar o projeto. O notebook pode ser aberto no
Jupyter/VS Code com Python 3 ou no Google Colab. Instale as dependências no kernel
selecionado e execute as células de cima para baixo. No Colab, a preparação pode
clonar o repositório público para obter as entradas; a execução dos estudos exige
enviar seus notebooks pessoais separadamente.

O pacote `rascunhos/saidas/atividade_5/atividade_5_entrega.zip` inclui notebook,
entradas, dependências e tabelas. As figuras estão incorporadas nas saídas do notebook;
executá-lo recria também os arquivos de imagens resultantes. O pacote não inclui aulas,
soluções pessoais ou exercícios. Para usar no Colab, extraia o ZIP em
`/content/VC_iREDE` e abra o notebook.
Se entregar apenas um link do Colab, confirme acesso de visualização liberado.

## Frentes pessoais, ignoradas pelo Git

- `rascunhos/atividade_5_gabarito.ipynb`: aula completa com matemática e exemplos.
- `rascunhos/laboratorios/atividade_5.ipynb`: sete implementações para tentar sozinho.
- `rascunhos/aulas/atividade_5_*.md`: fontes legíveis dos três notebooks.
- `rascunhos/saidas/atividade_5/`: exploração e verificações técnicas.

O laboratório não importa a solução de entrega e não a modifica. O gerador recusa
sobrescrever um laboratório existente. Para estudar, abra o notebook; não precisa
recriá-lo. Salve suas tentativas com Ctrl+S e faça uma cópia pessoal dos rascunhos.

Esta atividade continua temporariamente ignorada no Git, conforme a organização
de publicação já adotada. Para publicá-la depois, libere os padrões da atividade 5
em `.gitignore`; `rascunhos/` permanece ignorado.

Para validar e atualizar o ZIP desta revisão, execute na raiz:

```text
python rascunhos/ferramentas/validar_atividade_5.py --integridade rascunhos/saidas/atividade_5/integridade_simplificacao_20261025.json
```

A linha de base da revisão preserva o histórico anterior e verifica os arquivos que
não foram colocados em edição, inclusive originais, Atividade 4 e laboratório pessoal.

A versão anterior da entrega e suas tabelas de matching/robustez foram preservadas
em `rascunhos/arquivo/atividade_5_antes_simplificacao_20261025/`.
