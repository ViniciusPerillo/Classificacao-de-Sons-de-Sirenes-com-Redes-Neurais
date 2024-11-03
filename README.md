# Classificação de Sons de Sirenes com Redes Neurais (CNN e LSTM)

## Descrição

Este projeto foi desenvolvido como parte de um trabalho acadêmico para a disciplina de **Aprendizado de Máquina II** do curso de **Ciência da Computação** na Universidade Federal de São Carlos. O objetivo do projeto é construir e comparar modelos de redes neurais convolucionais (CNNs) e redes neurais recorrentes (LSTMs) para a classificação de sons de sirenes, incluindo sons de ambulâncias, caminhões de bombeiro e tráfego em geral.

## Equipe

- **Ana Ellen Deodato P Silva** - RA: 800206
- **Vinicius de Oliveira Guimarães** - RA: 802431
- **Vinícius Gonçalves Perillo** - RA: 800219

## Objetivo

Desenvolver um modelo de rede neural capaz de classificar diferentes tipos de sirenes a partir de espectrogramas dos áudios, utilizando técnicas de processamento de som, aumento de dados e redes neurais avançadas.

## Dados

Os dados utilizados neste projeto consistem em arquivos de áudio das classes:

- Ambulância (`ambulance`)
- Caminhão de bombeiros (`firetruck`)
- Tráfego (`traffic`)

A base contém 200 arquivos de áudio para cada classe, que foram divididos em 75% para treino e 25% para teste.

## Pré-processamento

1. **Conversão para Espectrograma Mel**: Transformação dos arquivos de áudio em espectrogramas Mel, que representam o som em três dimensões (tempo, frequência e amplitude).
2. **Aumento de Dados**: Aplicação de técnicas de aumento de dados, como `Gaussian Noise`, `Pink Noise` e `Random Gain`, para melhorar a generalização dos modelos.

## Modelos Implementados

Quatro abordagens foram testadas:

1. **CNN 2D sobre Espectrogramas Mel**: Rede convolucional profunda com 16 camadas para detecção de padrões nos espectrogramas.
2. **LSTM sobre Áudios**: Rede recorrente para captura de dependências temporais nos áudios.
3. **CNN 1D + LSTM**: Combinação de CNN 1D com LSTM diretamente sobre os áudios.
4. **CNN 2D + LSTM sobre Espectrogramas Mel**: Integração de CNN 2D e LSTM para processar os espectrogramas Mel.

## Resultados

| Modelo                         | Acurácia |
|--------------------------------|----------|
| CNN 2D sobre Espectrogramas Mel | 96.00%   |
| LSTM sobre os áudios            | 33.33%   |
| CNN 1D + LSTM com áudio         | 95.33%   |
| CNN 2D + LSTM com Espectrogramas Mel | 98.00% |

A melhor acurácia foi obtida com o modelo CNN 2D + LSTM sobre espectrogramas Mel, atingindo uma taxa de 98%.

## Conclusão

As CNNs se mostraram eficazes na extração de padrões dos espectrogramas, enquanto a combinação de CNN e LSTM melhorou a performance ao lidar com as dependências temporais dos dados. 

## Referências

- [Dataset no Kaggle](https://www.kaggle.com/datasets/vishnu0399/emergency-vehicle-siren-sounds)
- [Artigo sobre BirdCLEF e Mel Spectrograms](https://ceur-ws.org/Vol-3180/paper-174.pdf)

--- 

Essa estrutura resume o conteúdo do relatório em um formato claro e informativo, adequado para um README de repositório.