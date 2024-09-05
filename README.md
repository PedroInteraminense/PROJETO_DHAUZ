# Análise de Sentimentos em Viagens Aéreas

Este projeto foi desenvolvido para a DHAU, a base de dados foi retirada de um site que contém uma plataforma de venda de passagens aéreas, com o objetivo de implementar um sistema de **análise de sentimentos** a partir das avaliações de passageiros. A análise permitirá que as companhias aéreas identifiquem áreas de melhoria na experiência do cliente.

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

## Metodologia

O projeto consiste em duas abordagens principais de classificação de sentimentos:

1. **Análise baseada no texto**: Utiliza o texto das reviews e do título da avaliação como entrada para um modelo de classificação de sentimentos.
2. **Análise baseada nas notas das features**: Utiliza as notas individuais fornecidas pelos passageiros para características como conforto do assento, serviço da equipe, entretenimento a bordo, entre outras.

## Avaliação de Resultados

O desempenho do sistema será avaliado em termos de:

- **Classificação de Sentimento**:
  - Nota final < 4: Negativo
  - Nota final entre 4 e 7: Neutro
  - Nota final > 7: Positivo

- **Impacto dos atrasos no NPS**: Medir como atrasos no voo afetam a satisfação dos passageiros e o NPS das companhias aéreas, calculado como a diferença entre a porcentagem de avaliações positivas e negativas.

## Contribuição

Contribuições são bem-vindas! Para sugerir melhorias ou correções, abra uma issue ou faça um pull request.

---

**Autor**: [Seu Nome]  
**Empresa**: DHAUZ  
**Contato**: seuemail@demail.com
