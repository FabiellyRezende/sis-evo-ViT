# Comparação entre versões do Vision Transformer (ViT) em classificação de imagens

## Sobre o projeto

Este projeto foi desenvolvido com o objetivo de comparar o desempenho de diferentes versões do Vision Transformer (ViT) em tarefas de classificação de imagens.

O experimento foi realizado utilizando imagens de animais obtidas via URLs públicas, analisando o desempenho dos modelos em termos de:

- Precisão das classificações
- Tempo de inferência
- Consistência das predições
- Relação entre complexidade do modelo e desempenho

## Versões analisadas

As seguintes versões do Vision Transformer foram utilizadas nos experimentos:

- ViT-Base (google/vit-base-patch16-224)
- ViT-Large (google/vit-large-patch16-224)

## Metodologia

Foram selecionadas seis imagens contendo diferentes animais para avaliação dos modelos. Cada imagem foi processada individualmente por ambas as versões do ViT, permitindo comparação direta entre desempenho e resultados.

Durante a execução, foram coletadas as seguintes informações:

- Classe predita pelo modelo
- Probabilidade associada às previsões
- Tempo de inferência de cada modelo

Os resultados foram organizados em uma tabela comparativa para análise.

## Tecnologias utilizadas

- Google Colab
- PyTorch
- Transformers (Hugging Face)
- Pillow (PIL)
- ViT (Vision Transformer)

## Como executar

1. Abra o notebook no Google Colab ou ambiente Jupyter.

2. Instale as bibliotecas necessárias:

```bash
pip install transformers torchvision pillow torch
```

3. Execute o código para carregar os modelos ViT-Base e ViT-Large.

4. Insira as imagens via URL ou altere o link da variável:

```python
url = "LINK_DA_IMAGEM"
```

5. Execute a inferência para obter:
   - Classe predita
   - Probabilidades
   - Tempo de processamento


## Tabela comparativa
<img width="605" height="211" alt="image" src="https://github.com/user-attachments/assets/8e0fd611-2f70-4d73-98db-233057f87925" />



## Resultados

Os testes demonstraram diferenças significativas entre as versões do ViT. O modelo ViT-Base apresentou menor tempo de inferência, sendo mais rápido, enquanto o ViT-Large apresentou maior custo computacional.

Em relação à acurácia, ambos os modelos apresentaram bons resultados gerais, porém com algumas classificações incorretas dependendo da imagem analisada. Isso indica que o aumento da complexidade do modelo não garante necessariamente maior precisão em todos os casos.

## Conclusão

O experimento permitiu observar o trade-off entre desempenho computacional e complexidade do modelo. Enquanto o ViT-Large é mais robusto, o ViT-Base se destaca pela eficiência em tempo de processamento.

---
