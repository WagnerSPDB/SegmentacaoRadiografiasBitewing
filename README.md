# Auxílio ao Diagnóstico de Cáries

> **Sistema de segmentação automatizada de lesões em radiografias interproximais (Bitewing) utilizando Deep Learning.**

---

##  Descrição do Projeto

A cárie dentária é uma patologia bacteriana progressiva que compromete os tecidos duros do dente. Sua detecção precoce é crucial para evitar tratamentos invasivos e perda dentária. Este projeto surge como uma ferramenta de auxílio ao diagnóstico clínico, utilizando Visão Computacional para identificar e delimitar lesões com precisão.

Diferente de classificadores genéricos, nossa solução foca na **segmentação semântica**, mapeando a extensão da cárie pixel a pixel, proporcionando uma resposta visual detalhada para o cirurgião-dentista.

##  Metodologia

O pipeline do projeto foi desenhado para garantir rigor científico e eficiência computacional:

1.  **Extração e Isolamento (YOLO):** A partir da radiografia *Bitewing* bruta, utilizamos o modelo YOLO para detectar e extrair exclusivamente as regiões dos dentes, eliminando ruídos anatômicos (osso, gengiva e suportes).
2.  **Segmentação Pixel a Pixel (Deep Learning):** Os dentes isolados são processados por Redes Neurais Convolucionais especializadas em segmentação, que identificam áreas de desmineralização em nível de pixel.
3.  **Validação por Padrão-Ouro (Gold Standard):** Para garantir a confiabilidade, os resultados são comparados com máscaras reais anotadas manualmente por **estudantes de mestrado em Odontologia**, permitindo o cálculo preciso de métricas de desempenho (Dice Score, IoU, Sensibilidade e Especificidade).



##  Tecnologias Utilizadas

* **Linguagem:** Python
* **Deep Learning:** PyTorch / Torchvision
* **Visão Computacional:** OpenCV / YOLO (Ultralytics)
* **Aumentação de Dados:** Albumentations
* **Análise de Dados:** Pandas, Numpy, Matplotlib

##  Estrutura do Repositório

* `/data`: Scripts de carregamento e organização do dataset.
* `/notebooks`: Processo de Análise Exploratória e Treinamento.
* `/weights`: Pesos treinados dos melhores modelos.

##  Equipe e Instituição

* **Desenvolvedor:** Wagner Vasconcelos
* **Responsável:** Prof. Dr. Wellington Franco
* **Colaboração:** Programa de Pós-Graduação em Odontologia (Anotação Clínica)
* **Laboratório:** EngineLab

---
<p align="center">Desenvolvido como parte da pesquisa em Visão Computacioanl Aplicada à Saúde.</p>
