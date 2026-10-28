# 📘 Assignment: Python Data Visualization

## 🎯 Objective

Crie gráficos em Python com Matplotlib ou Plotly para explorar a participação em clubes escolares. Aprenda a escolher tipos de gráficos, adicionar elementos que facilitem a leitura e comunicar conclusões apoiadas nos dados.

## 📝 Tasks

### 🛠️ Crie seu primeiro gráfico de linhas

#### Descrição
Baixe [club-attendance.csv](./club-attendance.csv) e salve-o na mesma pasta do seu programa. O arquivo contém dados fictícios de participação mensal em três clubes; escolha Matplotlib ou Plotly e use a mesma biblioteca em todas as tarefas.

#### Requisitos
O programa concluído deve:

- Instalar a biblioteca escolhida com `python -m pip install matplotlib` ou `python -m pip install plotly`.
- Ler o arquivo com `csv.DictReader` da biblioteca padrão ou com pandas, caso também o instale; converter `participants` para valores numéricos.
- Criar um gráfico de linhas para o clube `Robotics`, com os seis meses em ordem cronológica no eixo horizontal e o número de participantes no eixo vertical.
- Adicionar título e rótulos aos dois eixos, deixando claro que os valores representam participantes.
- Usar os valores `12, 15, 14, 18, 22, 24` para `Robotics`, de janeiro a junho de 2026.

### 🛠️ Compare clubes e distribuições

#### Descrição
Amplie sua análise para comparar os três clubes. Escolha representações que permitam distinguir tendências mensais de diferenças na participação média.

#### Requisitos
O programa concluído deve:

- Expandir o gráfico de linhas para incluir `Robotics`, `Art` e `Chess`, com uma linha e uma entrada de legenda para cada clube.
- Distinguir as séries com cores e também com marcadores ou estilos de linha diferentes, sem depender apenas de cores.
- Criar um gráfico de barras com a média mensal de participantes de cada clube, calculada a partir dos seis registros correspondentes.
- Exibir as médias `17.5` para `Robotics`, `21.0` para `Art` e `12.5` para `Chess`, nos rótulos das barras ou nas informações ao passar o mouse.
- Iniciar em zero o eixo de valores do gráfico de barras e manter títulos e rótulos legíveis em ambos os gráficos.

### 🛠️ Exporte os gráficos e explique suas conclusões

#### Descrição
Prepare seus resultados para compartilhar com alguém que não executará o programa. Explique o que os gráficos mostram e quais conclusões não podem ser sustentadas apenas por esses dados.

#### Requisitos
O programa concluído deve:

- Salvar os dois gráficos como `attendance-trends.png` e `average-attendance.png` usando `savefig()` no Matplotlib, ou como `attendance-trends.html` e `average-attendance.html` usando `write_html()` no Plotly.
- Para Matplotlib, salvar com resolução mínima de 150 DPI e ajustar o layout para evitar rótulos cortados; para Plotly, gerar HTML independente com `include_plotlyjs=True`, que possa ser aberto sem conexão com a internet.
- Gerar `insights.txt` em UTF-8 com pelo menos duas conclusões numéricas: identificar o clube com maior média mensal e comparar o aumento de participantes de janeiro a junho entre os clubes.
- Explicar no relatório que a soma dos registros mensais não representa necessariamente pessoas únicas, pois uma mesma pessoa pode participar em vários meses.
- Conferir que os arquivos exportados abrem corretamente e incluem todos os clubes; entregar o programa, os dois gráficos e o relatório.

Como referência, `Art` tem a maior média mensal, com 21 participantes. De janeiro a junho, `Robotics` cresce 12 participantes, enquanto `Art` e `Chess` crescem 5 cada.
