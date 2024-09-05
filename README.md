# Análise de Sentimentos em Viagens Aéreas

Este projeto foi desenvolvido para a DHAUZ e a base de dados foi retirada de um site que contém uma plataforma de venda de passagens aéreas. O objetivo deste projeto é implementar um sistema de **análise de sentimentos** a partir das avaliações de passageiros. A análise permitirá que as companhias aéreas identifiquem áreas de melhoria na experiência do cliente.

## Objetivo

Criar um sistema que analise os reviews de passageiros para classificar o sentimento das avaliações (Positivo, Neutro, Negativo) e gerar insights sobre os principais pontos fortes e fracos da experiência de viagem. Além disso, será possível medir o impacto de variáveis como atrasos de voo na satisfação geral e no **NPS (Net Promoter Score)** das companhias aéreas.

## Base de Dados

A base de dados utilizada contém informações detalhadas sobre as avaliações de passageiros, incluindo:

- **Airline Name**: Nome da companhia aérea.
- **Overall_Rating**: Classificação geral da experiência do passageiro com a companhia aérea.
- **Review_Title**: Título da avaliação escrita pelo passageiro.
- **Review Date**: Data em que a avaliação foi publicada.
- **Review**: Texto completo da avaliação escrita pelo passageiro.
- **Aircraft**: Tipo de aeronave utilizada no voo.
- **Type Of Traveller**: Tipo de viajante (negócios, lazer).
- **Seat Type**: Tipo de assento (econômica, executiva).
- **Route**: Rota do voo (origem e destino).
- **Date Flown**: Data em que o voo foi realizado.
- **Seat Comfort**: Avaliação do conforto do assento.
- **Cabin Staff Service**: Avaliação do serviço da equipe de cabine.
- **Food & Beverages**: Avaliação da qualidade da comida e bebidas.
- **Ground Service**: Avaliação do serviço de solo.
- **Inflight Entertainment**: Avaliação do entretenimento a bordo.
- **Wifi & Connectivity**: Avaliação da qualidade do wifi e conectividade.

## QUESTÕES

### 1. Processamento dos Dados

- **Verificação de dados faltantes e duplicados**: O conjunto de dados será analisado para identificar valores ausentes ou duplicados que possam impactar a análise.
  
### 2. Pré-processamento de Texto (NLP)

Serão realizadas as seguintes etapas de processamento nas colunas `Review` e `Review_Title`:
- **Tokenização**: Separar as palavras em tokens.
- **Remoção de stop-words**: Excluir palavras irrelevantes (como "a", "o", "de").
- **Lemmatização/Stemming**: Redução das palavras à sua forma raiz.
- **Transformação para minúsculas**: Uniformizar as palavras.
  
### 3. Exploração dos Dados

#### a. Distribuição da feature `Overall_Rating`

- **Gráfico 1**: Distribuição do `Overall_Rating` por companhia aérea.
- **Gráfico 2**: Distribuição do `Overall_Rating` por modelo de aeronave (`Aircraft`).

#### b. Nuvem de Palavras

- **Análise 1**: Palavras mais frequentes em avaliações com `Overall_Rating` igual ou inferior a 3.
- **Análise 2**: Palavras mais frequentes em avaliações com `Overall_Rating` igual ou superior a 8.

#### c. Estudo de Correlação

Estudar a correlação entre as seguintes colunas e a nota final (`Overall_Rating`):
- `Seat Comfort`
- `Cabin Staff Service`
- `Food & Beverages`
- `Ground Service`
- `Inflight Entertainment`
- `Wifi & Connectivity`

### 4. Modelos de Classificação de Sentimento

Dois modelos de classificação de sentimentos serão desenvolvidos para comparar abordagens:

#### Modelo 1: Análise de Texto
Usará as colunas `Review` e `Review_Title` como input para a classificação de sentimentos, onde:
- Nota final < 4: **Negativo**
- Nota final entre 4 e 7: **Neutro**
- Nota final > 7: **Positivo**

#### Modelo 2: Análise Baseada em Features
Usará as notas das seguintes features:
- `Seat Comfort`
- `Cabin Staff Service`
- `Food & Beverages`
- `Ground Service`
- `Inflight Entertainment`
- `Wifi & Connectivity`

Os dois modelos serão comparados em termos de precisão na classificação de sentimentos.

### 5. Impacto dos Atrasos no NPS

Uma análise será realizada para avaliar o impacto dos atrasos de voo no **NPS** de 3 companhias aéreas. O cálculo do **NPS** será feito da seguinte forma:

- **NPS** = % avaliações **Positivas** - % avaliações **Negativas**

---

## Contribuição

Contribuições são bem-vindas! Para sugerir melhorias ou correções, abra uma issue ou faça um pull request.

---

**Autor**: Pedro Paulo B. Interaminense  
**Empresa**: DHAUZ  
**Contato**: pinteraminense@gmail.com
