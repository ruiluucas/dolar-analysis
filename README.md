# dolar-analysis — correlação do dólar (R)

Análise de correlação de séries cambiais em **R**, com ambiente reprodutível via **`renv`**.

## Estrutura

| arquivo | função |
|---|---|
| `correl.R` | script principal de correlação |
| `Dólar.Rproj` | projeto RStudio |
| `renv.lock` | **lockfile** — versões exatas dos pacotes |
| `.Rprofile` | ativação do renv no boot da sessão |
| `renv/` | biblioteca local isolada |

## Por que `renv`

`renv.lock` registra a **versão exata de cada pacote** usada na análise. Um ano depois, `renv::restore()`
reconstrói o ambiente idêntico — sem o clássico "funcionava na minha máquina".

Isso é a mesma disciplina de reprodutibilidade aplicada depois em Python: separar dado de código, fixar
versões, documentar fontes.

## Stack

`R` · `RStudio` · `renv`

## Rodar

```r
renv::restore()   # reconstrói o ambiente a partir do renv.lock
source("correl.R")
```

## Contexto

Exercício de 2023 de análise de correlação cambial em R — escolha da linguagem para praticar o ecossistema
estatístico, antes de consolidar o trabalho em Python.
