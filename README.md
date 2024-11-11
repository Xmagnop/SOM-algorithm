# Aplicação de Mapas Auto-Organizáveis (SOM) com e sem Bibliotecas

Este repositório contém implementações de Mapas Auto-Organizáveis (Self-Organizing Maps - SOM) aplicados ao dataset de vinhos. O SOM é uma técnica de aprendizado não supervisionado que organiza dados de alta dimensionalidade em um mapa bidimensional, facilitando a visualização e a identificação de padrões nos dados. Através de ajustes iterativos dos pesos, o SOM forma clusters e organiza os dados de maneira a revelar relações de similaridade entre amostras.

## Estrutura do Repositório

O jupyter notebook neste repositório (RoteiroEquipe-06SOM.ipynb) inclui:

- SOM Utilizando Biblioteca: Implementação do SOM usando a biblioteca MiniSom, que abstrai várias funções de inicialização, treinamento e mapeamento.
- SOM Manual: Implementação do SOM a partir do zero, sem bibliotecas externas, detalhando o processo de inicialização, treinamento, identificação do neurônio vencedor (BMU) e atualização dos pesos.

## Conceitos Principais

- Mapas Auto-Organizáveis (SOM): Redes neurais que organizam dados em uma estrutura bidimensional, preservando a topologia dos dados e agrupando amostras similares próximas umas das outras.
- BMU (Best Matching Unit): Neurônio vencedor, aquele que está mais próximo da amostra de entrada em termos de distância Euclidiana. É a unidade responsável por "representar" a amostra.
- Atualização dos Pesos: Após a identificação do BMU, ele e seus neurônios vizinhos ajustam seus pesos para se aproximar da amostra, organizando o mapa e formando clusters.
- Dataset de Vinhos: O dataset utilizado para esta análise consiste em informações químicas e sensoriais de diferentes tipos de vinhos, ideal para classificação não supervisionada.

## Estrutura de Implementação

Cada abordagem no notebook segue etapas semelhantes:

- Carregamento e Normalização dos Dados: O dataset de vinhos é carregado e normalizado para garantir que todos os atributos estejam em uma escala uniforme.
- Inicialização dos Pesos: Na implementação manual, os pesos são inicializados aleatoriamente dentro de um intervalo específico. Na implementação com biblioteca, essa etapa é realizada automaticamente.
- Treinamento da Rede SOM: Em ambas as implementações, o SOM é treinado iterativamente, atualizando os pesos dos neurônios próximos ao BMU.
- Visualização dos Clusters: Após o treinamento, o mapa SOM é visualizado com as amostras do dataset posicionadas em suas regiões correspondentes.

## Requisitos

Para executar o notebook, será necessário instalar as bibliotecas:
```
pip install numpy matplotlib scikit-learn minisom
```
