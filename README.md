# 📊 Análise de Sentimentos nas Avaliações da Saúde Pública
## Comparação entre BERTimbau e LSTM usando Processamento de Linguagem Natural (PLN)

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-DeepLearning-orange)
![Transformers](https://img.shields.io/badge/HuggingFace-Transformers-yellow)
![Status](https://img.shields.io/badge/Status-Concluído-green)

---

## 📌 Sobre o Projeto

A qualidade dos serviços públicos de saúde é um fator essencial para o bem-estar da população.  
Com o crescimento da digitalização, muitos cidadãos compartilham suas experiências por meio de avaliações online, que podem fornecer insights valiosos para gestores e formuladores de políticas públicas.

Este projeto tem como objetivo analisar avaliações de unidades de saúde pública em quatro cidades do estado de São Paulo:

- Cotia  
- Carapicuíba  
- Osasco  
- Itapevi  

Utilizando técnicas de **Processamento de Linguagem Natural (PLN)** para identificar sentimentos nos comentários.

Foram comparados dois modelos de Machine Learning:

- 🤖 BERTimbau (Transformer)
- 🔁 LSTM (Rede Neural Recorrente)

---

## 🎯 Objetivos

- Classificar sentimentos em avaliações de saúde pública
- Comparar desempenho entre BERTimbau e LSTM
- Aplicar a Roda das Emoções de Plutchik
- Identificar padrões de satisfação da população
- Demonstrar uso de IA em dados públicos

---

## 🗂️ Dataset de Treinamento

Foi utilizado o dataset **GoEmotions**, desenvolvido pelo Google.

- 211.226 frases
- 27 emoções
- Baseado na Roda de Plutchik
- Traduzido para português

### Pré-processamento

- Tradução para português
- Remoção de stopwords
- Correção ortográfica
- Balanceamento de classes
- Limpeza de texto
- Padronização

---

## 🏥 Dataset das Avaliações Públicas

Coleta realizada via **Web Scraping no Google Avaliações**

- 4 cidades
- 103 unidades de saúde
- 4.766 avaliações

### Tratamento dos dados

- Remoção de stopwords
- Correção ortográfica
- Normalização
- Limpeza de caracteres

---

## 🤖 Modelos Utilizados

### 🔹 BERTimbau

- Baseado em BERT
- Treinado para português
- Melhor compreensão semântica
- Melhor desempenho geral

### 🔹 LSTM

- Rede neural recorrente
- Boa para sequências
- Menor custo computacional
- Sensível a desbalanceamento

---

## 😊 Classificação de Sentimentos

Baseado na Roda das Emoções de Plutchik:

- Alegria
- Antecipação
- Raiva
- Tristeza
- Surpresa
- Nojo
- Medo
- Confiança

Também agrupado em:

- Positivo
- Neutro
- Negativo

---

## 📊 Resultados

✅ BERTimbau teve melhor precisão  
✅ Melhor desempenho em emoções raras  
⚠️ LSTM teve dificuldade com classes desbalanceadas  

### Tempo de treinamento

| Modelo | Tempo |
|--------|--------|
| BERTimbau | 40.21 min |
| LSTM | 28.3 min |

---

## 📈 Insights

- Maioria das avaliações positivas
- Muitos elogios ao atendimento
- Principais críticas:
  - Infraestrutura
  - Demora
  - Organização
  - Gestão

---

## 📌 Conclusões

- IA pode monitorar serviços públicos
- BERTimbau foi mais robusto
- PLN extrai insights de texto
- Feedback digital ajuda decisões públicas

---

## 💻 Tecnologias

- Python
- TensorFlow
- Keras
- Transformers
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Jupyter Notebook
- Web Scraping

---

## 📂 Estrutura do Projeto

```
projeto-analise-sentimentos/
│
├── datasets/
├── notebooks/
├── modelos/
├── resultados/
├── scraping/
├── preprocessing/
├── lstm/
├── bertimbau/
│
└── README.md
```

---

## 👨‍💻 Autor

Gustavo de Andrade Silva  
Projeto de Ciência de Dados  
Análise de Sentimentos com PLN

---
