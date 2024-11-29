Classificação de Feijões com Transfer Learning 🌱📸
Este projeto aplica Transfer Learning utilizando o modelo pré-treinado InceptionV3 para classificar imagens do dataset Beans em três categorias:

Saudável 🟢

Mancha Angular da Folha ⚠️

Ferrugem do Feijão 🔴

O objetivo é identificar doenças em feijões a partir de imagens tiradas em campo com smartphones, demonstrando o potencial de redes neurais profundas para resolver problemas no setor agrícola.

🔍 Visão Geral
Dataset: [Beans Dataset](https://www.tensorflow.org/datasets/catalog/beans?hl=pt-br)
3 Classes: Saudável, Mancha Angular da Folha e Ferrugem do Feijão
Tamanho: ~1.2k imagens divididas em treino, validação e teste
Modelo Utilizado: [InceptionV3](https://keras.io/api/applications/inceptionv3/) (pré-treinado no ImageNet)
Tecnologias:
Python 🐍
TensorFlow/Keras
Google Colab
 
⚙️ Etapas do Projeto:
1️⃣ Configuração do Ambiente
O ambiente foi configurado no Google Colab devido ao suporte a GPU e facilidade de execução. O dataset foi carregado diretamente via TensorFlow Datasets (TFDS).

2️⃣ Pré-processamento
As imagens foram redimensionadas para 150x150 pixels e normalizadas para o intervalo [0, 1], otimizando o desempenho do modelo durante o treinamento.

3️⃣ Transfer Learning com InceptionV3
O modelo pré-treinado InceptionV3 foi carregado com pesos do ImageNet, e sua arquitetura foi adaptada:

Camadas superiores descongeladas nas últimas épocas.
Nova camada densa para classificar as 3 classes do dataset Beans.
4️⃣ Treinamento do Modelo
Treinamos o modelo com:
Otimizador Adam com taxa de aprendizado ajustada.
Função de perda Sparse Categorical Crossentropy.
Conjunto de dados dividido em treino, validação e teste.
Realizamos 10 épocas de treinamento para refinar o desempenho.

5️⃣ Resultados do Treinamento
Época	Train Accuracy	Train Loss	Val Accuracy	Val Loss
1	56.04%	0.9375	76.69%	0.5166
5	91.37%	0.2502	84.96%	0.3487
10	95.35%	0.1370	88.72%	0.2921

6️⃣ Visualização de Predições
Abaixo estão exemplos de predições realizadas pelo modelo:
Imagem	Classe Predita	Confiança (%)
Saudável	98.7%
Ferrugem	95.3%

📊 Conclusão
Este projeto demonstrou que o Transfer Learning com InceptionV3 é uma abordagem eficiente para classificação de imagens em problemas específicos, mesmo com datasets limitados. Com acurácia de 88,72% no conjunto de validação, este modelo tem o potencial de ser implementado em sistemas agrícolas para:
Detecção precoce de doenças 🌾
Auxílio na tomada de decisão no campo 🛠️

📬 Contato
Se tiver dúvidas ou sugestões, sinta-se à vontade para entrar em contato!

Autor: Kaique Coutinho

LinkedIn: https://www.linkedin.com/in/kaique-coutinho/

Email: kaiquecoutinho200@gmail.com
