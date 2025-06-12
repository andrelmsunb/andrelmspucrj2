# README - Projeto Student Performance Analysis

## ANDRE LUIZ MARQUES SERRANO
## MVP2

## Análise Exploratória e Pré-processamento de Dados
### Dataset: Student Performance (UCI ML Repository)
---
##  Objetivo do Projeto

Este projeto realiza uma análise exploratória completa e pré-processamento de dados do dataset "Student Performance" do UCI Machine Learning Repository, seguindo os requisitos acadêmicos para desenvolvimento de MVP em ciência de dados.

**Problema**: Predizer o desempenho acadêmico final (G3) dos estudantes com base em características pessoais, familiares e escolares.
---
##  Estrutura do Projeto
```
student_performance_project/
├──  README.md                           # Este arquivo
├──  notebook_student_performance.ipynb  # Notebook principal (Jupyter)
├──  relatorio_final.md                  # Relatório detalhado
├──  Dados/
│   ├── student-mat.csv                    # Dataset original (Matemática)
│   ├── student-por.csv                    # Dataset original (Português)
│   ├── student.txt                        # Documentação das variáveis
│   ├── dataset_original.csv               # Dataset limpo
│   ├── dataset_basic.csv                  # Com encoding básico
│   ├── dataset_scaled.csv                 # Com normalização
│   └── dataset_complete.csv               # Versão completa processada
├──  Scripts/
│   ├── exploratory_analysis.py            # Análise exploratória
│   ├── create_visualizations.py           # Geração de gráficos
│   └── preprocessing.py                   # Pré-processamento
└──  Visualizações/
    ├── distribuicao_g3.png               # Distribuição da variável target
    ├── matriz_correlacao.png             # Matriz de correlação
    ├── distribuicoes_numericas.png       # Distribuições numéricas
    ├── distribuicoes_categoricas.png     # Distribuições categóricas
    ├── g3_por_categoricas.png            # G3 por categorias
    └── analise_outliers.png              # Análise de outliers
```
##  Resumo dos Resultados

### Dataset Analisado
- **Instâncias**: 395 estudantes
- **Variáveis**: 33 (30 features + 3 notas)
- **Qualidade**: Sem valores faltantes
- **Fonte**: Escolas portuguesas (Gabriel Pereira e Mousinho da Silveira)

### Principais Insights
- **Correlação mais forte com G3**: G2 (0.905), G1 (0.801)
- **Fator negativo**: Reprovações anteriores (-0.360)
- **Distribuição de performance**: 48.6% médio, 32.9% baixo, 18.5% alto
- **Diferença por aspiração**: Estudantes que querem ensino superior têm 3.81 pontos a mais

### Transformações Realizadas
-  **Encoding**: Label encoding (13 vars) + One-hot encoding (4 vars)
-  **Normalização**: Z-score para 13 variáveis numéricas
-  **Feature Engineering**: 4 novas variáveis derivadas
-  **Categorização**: G3_category para classificação
-  **Detecção de Outliers**: Método IQR aplicado
---
##  Como Executar

### 1. Pré-requisitos
```bash
pip install pandas numpy matplotlib seaborn scikit-learn scipy
```
### 2. Executar Análise Completa
```bash
# Análise exploratória
python exploratory_analysis.py

# Criar visualizações
python create_visualizations.py

# Pré-processamento
python preprocessing.py
```
### 3. Notebook Jupyter
```bash
jupyter notebook notebook_student_performance.ipynb
```
##  Principais Visualizações

### 1. Distribuição da Variável Target (G3)
- Histograma e boxplot da nota final
- Média: 10.42, Mediana: 11.00
- Distribuição aproximadamente normal

### 2. Matriz de Correlação
- Correlações entre todas as variáveis numéricas
- Identificação dos preditores mais importantes
- Visualização de padrões de relacionamento

### 3. Análise por Grupos
- Performance por variáveis categóricas
- Diferenças significativas identificadas
- Insights para intervenções educacionais

##  Metodologia Seguida

### 1. Definição do Problema
- [x] Problema de aprendizado supervisionado
- [x] Abordagem: Regressão e Classificação
- [x] Hipóteses formuladas e testadas

### 2. Análise Exploratória
- [x] Estatísticas descritivas completas
- [x] Verificação de qualidade dos dados
- [x] Visualizações informativas
- [x] Análise de correlações

### 3. Pré-processamento
- [x] Tratamento de variáveis categóricas
- [x] Normalização de variáveis numéricas
- [x] Criação de features derivadas
- [x] Detecção e análise de outliers

### 4. Preparação para Modelagem
- [x] 4 versões diferentes do dataset
- [x] Dados prontos para algoritmos ML
- [x] Documentação completa das transformações
---
##  Próximos Passos Recomendados

### 1. Modelagem
- Implementar modelos de regressão (Random Forest, XGBoost)
- Testar classificação para G3_category
- Aplicar validação cruzada
- Comparar performance entre datasets

### 2. Feature Selection
- Aplicar técnicas de seleção de features
- Testar importância com modelos tree-based
- Considerar PCA para redução de dimensionalidade

### 3. Interpretabilidade
- Usar SHAP values para explicabilidade
- Criar dashboard interativo
- Desenvolver recomendações acionáveis
---
## Referências

1. **Cortez, P. & Silva, A. (2008)**. Using data mining to predict secondary school student performance. *Proceedings of 5th Annual Future Business Technology Conference*.

2. **UCI Machine Learning Repository**. Student Performance Dataset. Disponível em: https://archive.ics.uci.edu/dataset/320/student+performance

3. **Documentação das Variáveis**: Ver arquivo `student.txt` para descrição completa de todas as 33 variáveis.

## Informações do Projeto

- **Autor**: ANDRE LUIZ MARQUES SERRANO
- **Data**: Junho 2025
- **Tipo**: MVP2 - Análise Exploratória e Pré-processamento
- **Linguagem**: Python 3.11
- **Bibliotecas**: pandas, numpy, matplotlib, seaborn, scikit-learn




