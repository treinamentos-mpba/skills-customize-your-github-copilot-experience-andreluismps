# 📘 Assignment: Python Text Processing

## 🎯 Objective

Crie um analisador de texto em Python para praticar manipulação de strings, leitura e escrita de arquivos. Ao final, você será capaz de normalizar palavras, calcular estatísticas e salvar versões transformadas de um texto.

## 📝 Tasks

### 🛠️ Normalize uma frase

#### Descrição
Comece com uma frase armazenada em uma variável e transforme-a em uma lista de palavras normalizadas. Use apenas a biblioteca padrão do Python.

#### Requisitos
O programa concluído deve:

- Remover espaços das extremidades da frase e converter o texto para letras minúsculas.
- Separar as palavras usando `split()` sem argumentos, tratando espaços repetidos e tabulações como separadores.
- Remover a pontuação das extremidades de cada palavra com `strip(string.punctuation)` e descartar resultados vazios; preserve a pontuação interna das palavras.
- Exibir a lista de palavras e sua quantidade. Uma entrada vazia ou composta apenas de pontuação deve produzir uma lista vazia e contagem zero.

Exemplo de entrada:

```text
  Python,   makes TEXT processing fun!
```

Saída esperada:

```text
['python', 'makes', 'text', 'processing', 'fun']
Total de palavras: 5
```

### 🛠️ Leia e analise um arquivo de texto

#### Descrição
Baixe [sample.txt](./sample.txt) e salve-o na mesma pasta do seu programa. Reutilize a normalização da primeira tarefa para analisar todo o arquivo.

#### Requisitos
O programa concluído deve:

- Abrir `sample.txt` para leitura com `with open(...)` e `encoding="utf-8"`.
- Contar as linhas com `splitlines()`, incluindo linhas vazias existentes no texto; um arquivo vazio deve ter zero linhas.
- Calcular o total de palavras normalizadas, a quantidade de palavras únicas e a frequência de cada palavra.
- Exibir as cinco palavras mais frequentes, ordenadas por frequência decrescente e, em caso de empate, por ordem alfabética. Se houver menos de cinco palavras únicas, exibir todas.
- Para o arquivo fornecido, obter 3 linhas, 14 palavras e 10 palavras únicas, com `makes`, `practice`, `python` e `text` aparecendo duas vezes cada.
- Se o arquivo não existir, exibir uma mensagem clara com seu nome e encerrar sem gerar resultados ou arquivos de saída.

As cinco palavras mais frequentes do exemplo devem ser:

```text
makes: 2
practice: 2
python: 2
text: 2
files: 1
```

### 🛠️ Transforme o texto e salve um relatório

#### Descrição
Gere uma versão modificada do texto e um relatório com as estatísticas. Mantenha o arquivo original intacto para poder comparar os resultados.

#### Requisitos
O programa concluído deve:

- Substituir todas as ocorrências exatas de `Python` por `Python 3` no texto original usando `replace()`. A substituição deve diferenciar maiúsculas de minúsculas.
- Salvar o resultado em `transformed.txt` e as estatísticas da segunda tarefa em `report.txt`, usando `with open(...)` e `encoding="utf-8"` para ambos.
- Incluir no relatório o número de linhas, o total de palavras, o número de palavras únicas e a lista das cinco palavras mais frequentes do texto original, antes da substituição.
- Sobrescrever os arquivos de saída a cada execução, sem acumular relatórios anteriores e sem modificar `sample.txt`.
- Verificar o programa com o arquivo fornecido, um arquivo vazio e um texto com espaços repetidos e pontuação. Para um arquivo vazio, salvar um texto transformado vazio e um relatório com contagens zero e nenhuma palavra na lista de frequências.

A primeira linha de `transformed.txt` para o arquivo fornecido deve ser:

```text
Python 3 makes text processing fun.
```
