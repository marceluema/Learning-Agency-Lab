Modelo de Previsão de Notas de Redações usando Random Forest Este projeto utiliza Random Forest para prever as notas de redações do desafio "Learning Agency Lab - Automated Essay Scoring 2.0" do Kaggle. O modelo foi treinado utilizando características extraídas dos textos, como:

Comprimento do Texto Quantidade de Erros Gramaticais (utilizando language_tool_python) Diversidade Lexical (utilizando spaCy) O projeto tem como objetivo explorar os desafios e limitações na avaliação automática de redações, utilizando um modelo Random Forest Classifier.

📊 Resultados Obtidos O modelo alcançou uma acurácia de 49%, o que destacou desafios importantes, como:

Limitações das variáveis utilizadas para capturar a complexidade da avaliação humana. Falta de contexto semântico e análise de coerência nas redações. Desbalanceamento das classes, com algumas notas tendo menos amostras. 🛠️ Tecnologias Utilizadas Python Pandas para manipulação de dados. spaCy para processamento de linguagem natural. LanguageTool-python para verificação gramatical. Scikit-learn para o modelo Random Forest e avaliação de desempenho. 📁 Estrutura do Projeto r Copiar Editar ├── README.md <- Documentação do projeto
├── train.csv <- Dataset usado para treinamento e teste
└── random_forest_model.py <- Script principal com o modelo Random Forest
🚀 Como Executar o Projeto Pré-requisitos Certifique-se de ter o Python 3.7+ instalado em sua máquina. Instale as dependências necessárias utilizando:

bash Copiar Editar pip install pandas spacy numpy language_tool_python scikit-learn Configuração do spaCy Baixe o modelo de linguagem do spaCy utilizando:

bash Copiar Editar python -m spacy download en_core_web_sm Executando o Script Coloque o arquivo train.csv na pasta do projeto. Execute o script utilizando: bash Copiar Editar python random_forest_model.py O script irá:

Carregar o dataset train.csv Extrair as características das redações (comprimento do texto, erros gramaticais e diversidade lexical) Treinar um Random Forest Classifier Avaliar o modelo com base na acurácia e imprimir um relatório de classificação 📝 Funcionalidades Extração de Características: Comprimento do texto, quantidade de erros gramaticais e diversidade lexical. Treinamento do Modelo: Utiliza Random Forest para prever as notas das redações. Avaliação do Modelo: Calcula acurácia e gera um relatório de classificação detalhado. Previsão de Notas: Função para prever a nota de um novo texto inserido pelo usuário. 🔍 Exemplos de Uso Você pode utilizar a função predict_score() para prever a nota de uma redação inédita:

python Copiar Editar example_text = "This is a sample essay text." predicted_score = predict_score(example_text) print(f"A nota prevista é: {predicted_score}") 📊 Resultados e Desafios Acurácia Obtida: 49% Desafios Identificados: Limitação das variáveis utilizadas. Falta de análise de coerência e contexto semântico. Desbalanceamento das classes no dataset.

Learning_Agency_Lab/README.md at main · marceluema/Learning_Agency_Lab
