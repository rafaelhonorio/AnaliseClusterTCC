# Análise de Clusters com K-Prototypes

Este projeto realiza uma análise exploratória e clustering em dados de um questionário aplicado a estudantes da UnB, utilizando o algoritmo **K-Prototypes** (adequado para dados mistos: numéricos e categóricos). O objetivo é identificar agrupamentos semelhantes de estudantes com base em variáveis como idade, tempo de deslocamento, tipo de escola cursada e conhecimento prévio em programação.

## ✍️ O que este projeto faz?

- Pré-processa dados de um arquivo Excel (`tabela_clusters.xlsx`), renomeando colunas e realizando padronização (scaling) das variáveis numéricas.
- Utiliza o método do cotovelo para sugerir o número ideal de clusters.
- Aplica o algoritmo **K-Prototypes** para agrupar os dados.
- Realiza redução de dimensionalidade com **TSNE** para visualização em 2D.
- Cria gráficos interativos em Plotly (Scatter, Boxplot e Violin plots) para entender o comportamento das variáveis nos diferentes clusters.
- Salva os resultados em um novo arquivo Excel com a coluna de cluster atribuída.

## 🚀 Como executar

1. Clone o repositório:
   ```bash
   git clone https://github.com/seu-usuario/seu-repo.git
   cd seu-repo
2. Instale as dependências (preferencialmente num ambiente virtual):
  pip install pandas numpy matplotlib plotly scikit-learn kmodes

3. Ajuste o caminho do arquivo de dados:
No script analise.py, edite:
  df = pd.read_excel("/content/drive/MyDrive/tabela_clusters.xlsx", sheet_name="base toda")
para apontar para o local onde está o seu arquivo tabela_clusters.xlsx.

4. Execute o script:
  python analise.py

💡 Este script foi inicialmente desenvolvido no Google Colab e contém comandos específicos como drive.mount('/content/drive'). Caso execute localmente, remova ou adapte estas linhas.

📊 Bibliotecas utilizadas
pandas e numpy para manipulação e análise de dados
scikit-learn para padronização e TSNE
kmodes para clustering com K-Prototypes
matplotlib e plotly para visualizações

📝 Principais arquivos
analise.py : Script principal com todo o pipeline de pré-processamento, clustering e visualização.
tabela_clusters.xlsx : Arquivo esperado com os dados originais (não incluído no repositório).

🔍 Resultados
O script gera:

Gráficos do método do cotovelo para escolha de k.
Visualização em 2D via TSNE destacando os clusters.
Boxplots e Violin plots para comparar distribuições das variáveis entre os clusters.
Um novo arquivo Excel com o cluster atribuído a cada registro.
