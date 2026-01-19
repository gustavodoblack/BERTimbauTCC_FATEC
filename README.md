# BERTimbauTCC_FATEC
Projeto de dados para análise de sentimentos comparando os modelos BERTimbau e LSTM para Processamento de Linguágem Natural (PLN).
Análise de Sentimentos nas Avaliações da Saúde Pública
Projeto de Ciência de Dados – Comparação entre BERTimbau e LSTM
Resumo do Projeto:

A qualidade dos serviços públicos de saúde é um fator essencial para o bem-estar da população. Com o crescimento da digitalização, muitos cidadãos compartilham suas experiências por meio de avaliações online, que podem fornecer insights valiosos para gestores e formuladores de políticas.

Este projeto tem como objetivo analisar as avaliações das unidades de saúde pública em quatro cidades do estado de São Paulo (Cotia, Carapicuíba, Osasco e Itapevi), utilizando técnicas de Processamento de Linguagem Natural (PLN) para identificar os sentimentos expressos nos comentários.*

Para isso, foram comparados dois modelos de aprendizado de máquina: BERTimbau, um modelo baseado em Transformer treinado para a língua portuguesa, e LSTM (Long Short-Term Memory), uma rede neural recorrente amplamente utilizada para processamento de sequências textuais.

Base de Dados Utilizada Para o Treinamento Dos Modelos: GoEmotions
Para treinar os modelos de Processamento de Linguagem Natural (PLN) na classificação de sentimentos, utilizamos a base de dados GoEmotions, desenvolvida pelo Google. Trata-se de um dataset de código aberto, amplamente utilizado na pesquisa de emoções em texto.

A GoEmotions contém um total de 211.226 sentenças, classificadas em 27 categorias emocionais com base na Roda das Emoções de Plutchik. Essa variedade permite que os modelos aprendam a distinguir sentimentos mais específicos além das emoções básicas. Adaptando-se para o Português.

Como a base de dados original está em inglês, foi necessário realizar um processo de tradução para garantir que os modelos fossem treinados em português. Além disso, aplicamos técnicas de pré-processamento, como:

✅ Tradução de textos para padronizar os comentários que estavam em inglês;
✅ Remoção de stopwords para eliminar palavras irrelevantes;
✅ Correção ortográfica para evitar ruídos nos dados;
✅ Balanceamento das classes para garantir que o modelo não fosse tendencioso a determinadas emoções.

Esses ajustes foram essenciais para que os modelos pudessem reconhecer sentimentos em textos escritos em português brasileiro, tornando a análise mais precisa e relevante para o contexto das avaliações.

Base de Dados Com As Avaliações Públicas:
A primeira etapa para a criação da base de dados com as avaliações das quatro cidades consistiu na coleta de avaliações públicas disponíveis no Google Avaliações, utilizando técnicas de Web Scraping. O dataset final contém 4.766 avaliações, de um total de 103 unidades de saúde divididos entre as 4 cidades.

Para garantir a qualidade dos dados, foram realizadas as seguintes etapas de pré-processamento:

✅ Remoção de Stopwords para eliminar palavras irrelevantes para a análise de sentimento.
✅ Correção ortográfica para evitar ruídos nos modelos de PLN.

Modelos Utilizados:
Após pesquisar sobre as possíveis opções, foram selecionados e treinados dois modelos distintos para a classificação de sentimentos:

🔹 BERTimbau: Baseado no modelo BERT, uma variação treinada especificamente para a língua portuguesa, permitindo uma compreensão mais precisa dos textos escritos no idioma.

🔹 LSTM (Long Short-Term Memory): Uma rede neural recorrente projetada para capturar padrões em textos. É amplamente utilizada para PLN devido à sua capacidade de manter memória de longo prazo em textos.

Classificação de Sentimentos:
Para categorizar os sentimentos expressos nos comentários, utilizou-se a Roda das Emoções de Plutchik, um modelo psicológico que classifica 27 emoções humanas e as agrupa em oito categorias principais:

🟢 Alegria
🟡 Antecipação
🔴 Raiva
🔵 Tristeza
🟠 Surpresa
🟣 Nojo
⚫ Medo
⚪ Confiança

Essas categorias principais também foram agrupadas com a clássica classificação Positiva, Neutra e Negativa, para avaliações mais abrangentes.

Resultados Obtidos:
Após a aplicação dos modelos de PLN ao dataset de avaliações de saúde pública, observamos os seguintes insights:

✅ O BERTimbau apresentou um desempenho superior, com maior precisão na classificação de sentimentos, principalmente em emoções menos frequentes no dataset.

✅ O modelo LSTM, apesar de ter conseguido se sair muito bem na classificação, teve dificuldades em identificar corretamente certos sentimentos, especialmente aqueles menos representados nos dados, mesmo após o balanceamento de classes.

✅ Análise Exploratória dos Comentários: É possível notar que a maioria das avaliações está ligada à qualidade positiva do atendimento, tanto em elogios quanto em agradecimentos. Isso sugere que os usuários que fizeram os comentários valorizam bastante a interação com os profissionais da saúde. Porém, parte significativa das avaliações estavam relacionadas a falta de qualidade nas unidades de saúde, como críticas a infraestrutura, atrasos nos atendimentos e a gestão de saúde num geral.

✅ O tempo de processamento dos modelos variou, sendo:

• ⏳ BERTimbau: 40,21 minutos
• ⏳ LSTM: 28,3 minutos

Conclusões e Impacto do Projeto:
📌 O uso de Inteligência Artificial aplicada à saúde pública permite extrair informações valiosas sobre a percepção da população em relação aos serviços oferecidos.
📌 O BERTimbau se mostrou uma alternativa mais robusta para a classificação de sentimentos em português, sendo uma ferramenta promissora para análises futuras.
📌 A análise indicou que, de forma sutil, os sentimentos expressos nas avaliações eram positivos, refletindo uma percepção favorável da população em relação aos serviços prestados pelas unidades de saúde estudadas.
📌 Com o crescimento da cultura do feedback digital, técnicas como PLN e aprendizado de máquina podem ser aplicadas para monitorar a satisfação dos cidadãos e auxiliar na tomada de decisões estratégicas para melhoria contínua dos serviços públicos.

Tecnologias Utilizadas:
💻 Linguagem de Programação: Python
📊 Bibliotecas: Transformers, BertTokenizer, TensorFlow, Keras, Matplotlib, Seaborn, NumPy, Pandas
📡 Coleta de Dados: Web Scraping
🤖 Modelos de Machine Learning: BERTimbau, LSTM
📂 Ambiente de Desenvolvimento: Jupyter Notebook

Acesse os arquivos para verificar outras informações do projeto:
Deixei alguns slides selecionados que ajudam no entendimento dos modelos e resultados.
No arquivo AlgoritmoBERT.ipynb se encontra o código python.
Os arquivos da pasta fine_tuned_model são utilizados para rodar o BERTimbau em python.
O arquivo RESULTADOS_BERT é a BASE_CIDADES com os resultados do BERTimbau.

Caso se interesse e queira entender melhor do projeto, entre em contato via Linkedin.
Obrigado
