#  Segmentação e Diagnóstico de Doenças em Folhas de Café com YOLOv8

Este projeto desenvolve uma solução de **Visão Computacional** baseada em Deep Learning para auxiliar a cafeicultura. O objetivo é realizar a segmentação de instância (recorte preciso da folha) e a classificação automática de doenças em ambientes de campo não controlados.

##  Objetivo
Desenvolver um modelo capaz de distinguir folhas de café do fundo complexo (terra, vegetação, interferências visuais) e identificar patógenos com alta precisão, focando na aplicabilidade real ("in the wild").

##  Tecnologias Utilizadas
* **Modelo:** YOLOv8-seg (You Only Look Once - Instance Segmentation).
* **Framework:** PyTorch & Ultralytics.
* **Hardware de Treino:** GPU NVIDIA (RTX Series).
* **Linguagem:** Python 3.

##  Dataset e Metodologia
Diferente de abordagens tradicionais que utilizam imagens em fundo branco (laboratório), este projeto utiliza o dataset **ROCOLE (Robusta Coffee Leaf)**.
* **Motivação:** O ROCOLE apresenta imagens capturadas em condições reais de campo, com variações de luz e fundo ruidoso, garantindo que a IA aprenda a generalizar para o mundo real.
* **Pré-processamento:** Foi realizada a unificação estratégica das classes de severidade da ferrugem para aumentar a robustez estatística do modelo.

### Classes Detectadas:
1.  **Healthy** (Folha Saudável)
2.  **Red Spider Mite** (Ácaro-vermelho)
3.  **Rust** (Ferrugem - *Hemileia vastatrix*)

##  Resultados Preliminares
O modelo utiliza a arquitetura **CNN (Rede Neural Convolucional)** de estágio único para prever simultaneamente a caixa delimitadora (bounding box) e a máscara de segmentação (mask), permitindo isolar a folha de interesse para análise agronômica.

---
*Projeto desenvolvido no contexto acadêmico de Engenharia Computacional.*
