# predicao-evasao-estudantil-ML-PP01
Este projeto aplica algoritmos de Aprendizagem Automática (Machine Learning) para prever a situação académica de estudantes do ensino superior, classificando-os em três categorias: Dropout (evasão), Enrolled (matriculados) e Graduate (formados). O objetivo é identificar precocemente estudantes em risco de abandono letivo, permitindo à instituição adotar medidas preventivas.

O estudo avalia o desempenho dos modelos k-Nearest Neighbors (k-NN) e da Árvore de Decisão ao longo de três cenários temporais (A, B e C), que representam diferentes momentos da trajetória académica do estudante (desde o ato da matrícula até ao final do primeiro ano letivo).

Estrutura do Repositório:
O projeto está dividido em vários *notebooks* modulares para facilitar a compreensão de cada etapa do processo de *Machine Learning*:

Pré-processamento:
  * `tirandoOutiliers.ipynb`: Análise e remoção de valores atípicos (outliers).
  * `pre_processamento_nominais.ipynb`: Aplicação de One-Hot Encoding para variáveis nominais.
  * `pre_processamento_ordinais.ipynb`: Codificação sequencial de variáveis ordinais.
  * `eliminacao_dos_3_atributos_e_divisao_de_cenario.ipynb`: Redução de dimensionalidade baseada na variância e separação dos dados nos cenários A, B e C.
Modelos:
  * `arvore_decisao_Cenario[A/B/C].ipynb`: Implementação, treino e teste do algoritmo de Árvore de Decisão para cada cenário (avaliando Gini e Entropia, com e sem PCA).
  * `kNNotimizadoCenario[A/B/C].ipynb`: Implementação, treino e teste do algoritmo k-NN para cada cenário (avaliando distâncias Euclidiana e Manhattan, com e sem PCA/Padronização).
  * 'codgeral' faz todo Pré-processamento mais o melhor resultando da arvore e knn no cenario C
  * Mais informações no nosso relatório do projeto: https://docs.google.com/document/d/1Y2Bg01xQD9L-oZFg2GH80OpBiDZ7vstcFDlXDFSkw6U/edit?usp=sharing

Tecnologias Utilizadas:
Linguagem: Python 3
Principais Bibliotecas: `pandas`, `numpy`, `scikit-learn`, `matplotlib`

Observação:
Os dados utilizados para o treino e teste dos modelos encontram-se em ficheiros `.csv` (ex: `cenarioA.csv`, `cenarioB.csv`, `semoutliers.csv`). É estritamente necessário alterar o caminho (path) de leitura dos ficheiros CSV no código, dependendo da diretoria onde guardou este repositório na sua máquina local. 
Antes de executar, procure as linhas de código com `pd.read_csv('...')` nos notebooks e ajuste o caminho para refletir a localização exata dos ficheiros no seu computador.

Como Executar:
1. Faça o clone deste repositório para a sua máquina local.
2. Certifique-se de que tem o Python instalado, bem como as bibliotecas listadas acima (pode instalá-las via `pip install pandas numpy scikit-learn matplotlib`).
3. Abra os notebooks (ficheiros `.ipynb`) utilizando o Jupyter Notebook, JupyterLab, VS Code ou Google Colab.
4. Verifique e altere os caminhos dos ficheiros `.csv` (conforme o aviso acima).
5. Execute as células de forma sequencial, começando pelos *notebooks* de pré-processamento e avançando para os de modelagem (`arvore_decisao` e `kNN`).

Autores:
Projeto desenvolvido no âmbito da disciplina de Aprendizado de Máquina do curso de Ciência da Computação da Universidade Federal do Ceará (UFC) - Campus Russas.
Davi Ramalho Castro Pinheiro
Felipe Rodrigues de Oliveira
Lucas José Sousa Lima
