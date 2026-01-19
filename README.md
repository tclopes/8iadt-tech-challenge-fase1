# Análise de Depressão e Violência Sexual em Mulheres Brasileiras

**Instituição:** FIAP - Pós-Graduação em Inteligência Artificial para Devs  
**Disciplina:** Tech Challenge IADT - Fase 1

## Sobre o Projeto

Este projeto realiza uma análise exploratória e preditiva da relação entre depressão e violência sexual em mulheres brasileiras, utilizando dados da **Pesquisa Nacional de Saúde (PNS) 2019** do IBGE. O estudo investiga como experiências de violência sexual se correlacionam com diagnósticos de depressão e atendimento psicológico.

## 📊 Fonte dos Dados

**Base de Dados:** Pesquisa Nacional de Saúde 2019 (PNS-2019) - IBGE
- **Arquivo Original:** pns-2019.csv (microdados brutos)
- **População Alvo:** Mulheres (filtrado por sexo feminino)
- **Amostra:** 144.940 registros de mulheres com 15 anos ou mais
- **Variáveis Originais:** Mais de 3.000 variáveis coletadas
- **Variáveis Selecionadas:** 21 variáveis relevantes para o estudo

## 🎯 Objetivo

Investigar a relação entre experiências de violência sexual e depressão em mulheres brasileiras através de:
1. Análise exploratória dos dados
2. Identificação de padrões e correlações
3. Desenvolvimento de modelos preditivos de machine learning
4. Comparação de diferentes algoritmos de classificação

## 📁 Estrutura do Projeto

```
.
├── 8IADT - Fase 1 - Tech challenge.pdf         # Descrição do desafio
├── 1-GeraArquivoReduzido.ipynb                 # Filtragem e seleção de variáveis
├── 2-AnaliseExploratoria.ipynb                 # Análise exploratória de dados (EDA)
├── 3-Regressão_logística_multivariada.ipynb    # Modelo de regressão logística
├── 4-Random_Forest.ipynb                       # Modelo Random Forest
├── 5-CATBOOST.ipynb                            # Modelo CatBoost
├── 6-ComparaModelos.ipynb                      # Comparação de desempenho dos modelos
├── Relatório Final.pdf                         # Relatório final
└── README.md                                   # Este arquivo
```

## 📋 Variáveis do Estudo

### Variável Alvo (Target)
- **Q092:** Depressão e atendimento psicológico

### Variáveis Demográficas e Socioeconômicas
- **C008:** Idade
- **C009:** Cor ou raça
- **D00301:** Escolaridade
- **C011:** Estado civil

### Variáveis de Saúde Física
- **P00104:** Peso corporal
- **P00404:** Altura
- **IMC:** Índice de Massa Corporal (calculado)

### Variáveis de Estilo de Vida
- **Q018013:** Prática de atividade física
- **P027:** Consumo de álcool
- **P050:** Tabagismo e frequência

### Variáveis de Violência Sexual (últimos 12 meses)
- **V02701:** Toque, manipulação, beijo ou exposição de partes do corpo contra vontade
- **V02702:** Ameaça ou relação sexual forçada

### Variáveis de Violência Sexual (alguma vez na vida)
- **V02801:** Toque, manipulação, beijo ou exposição de partes do corpo contra vontade
- **V02802:** Ameaça ou relação sexual forçada

### Variáveis de Contexto e Consequências
- **V029:** Frequência de ocorrência nos últimos 12 meses
- **V032:** Identificação do agressor
- **V033:** Local de ocorrência
- **V034:** Prejuízo nas atividades habituais devido à violência

### Variáveis de Consequências para Saúde
- **V03501:** Lesões físicas (hematomas, cortes, fraturas, queimaduras)
- **V03502:** Consequências psicológicas (medo, tristeza, desânimo, ansiedade, depressão)
- **V03503:** Doenças sexualmente transmissíveis ou gravidez indesejada

## 🔍 Análise Exploratória

A análise exploratória incluiu:

1. **Limpeza e Preparação dos Dados**
   - Tratamento de valores ausentes
   - Conversão de tipos de dados
   - Criação de variáveis derivadas (IMC, categorias de violência)

2. **Análise Descritiva**
   - Distribuição de variáveis demográficas
   - Prevalência de depressão
   - Frequência de experiências de violência sexual

3. **Análise de Correlação**
   - Correlação de Spearman entre variáveis numéricas
   - Heatmap de correlações
   - Identificação de relações significativas

4. **Visualizações**
   - Distribuições de idade, IMC e outras variáveis contínuas
   - Análise de frequências de variáveis categóricas
   - Gráficos de barras e histogramas

## 🤖 Modelos de Machine Learning

Foram desenvolvidos e comparados três modelos de classificação:

### 1. Regressão Logística Multivariada
- Modelo baseline para classificação binária
- Interpretabilidade dos coeficientes
- Análise da contribuição de cada variável

### 2. Random Forest
- Ensemble de árvores de decisão
- Análise de importância das features
- Robustez a outliers e não-linearidades

### 3. CatBoost
- Gradient boosting otimizado para variáveis categóricas
- Alta performance em dados tabulares
- Tratamento automático de missing values

### Métricas de Avaliação
- **Acurácia:** Proporção de predições corretas
- **Precisão:** Taxa de verdadeiros positivos dentre predições positivas
- **Recall (Sensibilidade):** Taxa de verdadeiros positivos identificados
- **F1-Score:** Média harmônica entre precisão e recall
- **AUC-ROC:** Área sob a curva ROC
- **Matriz de Confusão:** Distribuição de predições corretas e incorretas

## 📊 Principais Descobertas

### Correlações Identificadas
- Forte correlação entre diferentes tipos de violência sexual
- Associação entre consequências psicológicas de violência e depressão
- Relação entre frequência de violência e impacto na saúde mental

### Padrões Observados
- Distribuição etária da amostra
- Perfil socioeconômico das entrevistadas
- Prevalência de violência sexual em diferentes contextos

## 🛠️ Tecnologias Utilizadas

### Linguagem e Ambiente
- **Python 3.13.5**
- **Jupyter Notebook**
- **Conda** para gerenciamento de ambiente

### Bibliotecas Principais

#### Manipulação de Dados
- `pandas` - Análise e manipulação de dados
- `numpy` - Operações numéricas

#### Visualização
- `matplotlib` - Visualizações básicas
- `seaborn` - Visualizações estatísticas avançadas

#### Machine Learning
- `scikit-learn` - Modelos clássicos (Regressão Logística, Random Forest)
- `catboost` - Gradient boosting especializado
- `imbalanced-learn` - Técnicas para dados desbalanceados

#### Outras
- `math` - Funções matemáticas
- Métricas de avaliação (accuracy, precision, recall, f1-score, AUC-ROC)

## 📈 Como Utilizar

### Pré-requisitos
```bash
# Instalar conda (Anaconda ou Miniconda)
# Criar ambiente virtual
conda create -n depression_analysis python=3.13

# Ativar ambiente
conda activate depression_analysis

# Instalar dependências
pip install pandas numpy matplotlib seaborn scikit-learn catboost imbalanced-learn jupyter
```

### Executar a Análise

1. **Gerar Dataset Reduzido**
   ```bash
   jupyter notebook 1_GeraArquivoReduzido.ipynb
   ```
   - Certifique-se de ter o arquivo `pns-2019.csv` no mesmo diretório
   - Este notebook gerará `pns-2019_saude_mulher_filtrado.csv`

2. **Análise Exploratória**
   ```bash
   jupyter notebook 2_AnaliseExploratoria.ipynb
   ```
   - Explore as distribuições e correlações
   - Gere visualizações dos dados

3. **Treinar Modelos**
   ```bash
   # Regressão Logística
   jupyter notebook 3_Regressão_logística_multivariada.ipynb
   
   # Random Forest
   jupyter notebook 4_Random_Forest.ipynb
   
   # CatBoost
   jupyter notebook 5_CATBOOST.ipynb
   ```

4. **Comparar Modelos**
   ```bash
   jupyter notebook 6_ComparaModelos.ipynb
   ```
   - Analise métricas de desempenho
   - Compare resultados entre modelos

## 🎥 Vídeo Explicativo do Projeto

Para uma visão geral rápida e intuitiva sobre o funcionamento do projeto, assista ao vídeo explicativo no link abaixo:

[https://youtu.be/YgazGCn7200](https://youtu.be/YgazGCn7200)

## 🔐 Considerações Éticas

Este projeto trabalha com dados sensíveis sobre violência sexual e saúde mental. As seguintes considerações foram observadas:

1. **Confidencialidade:** Todos os dados são agregados e anonimizados pela PNS-IBGE
2. **Sensibilidade:** O tema requer tratamento respeitoso e científico
3. **Propósito:** Contribuir para o entendimento de questões de saúde pública
4. **Responsabilidade:** Resultados não substituem avaliação profissional

## ⚠️ Limitações do Estudo

- **Dados transversais:** Impossibilidade de estabelecer causalidade direta
- **Auto-relato:** Possível subnotificação de casos de violência
- **Fatores confundidores:** Variáveis não incluídas no modelo
- **Generalização:** Resultados específicos para a população brasileira em 2019
- **Desbalanceamento de classes:** Possível viés em favor da classe majoritária

## 📚 Referências

- Instituto Brasileiro de Geografia e Estatística (IBGE). **Pesquisa Nacional de Saúde 2019**. Disponível em: https://www.ibge.gov.br/estatisticas/sociais/saude/9160-pesquisa-nacional-de-saude.html

- Dicionário de variáveis da PNS 2019

## 👥 Equipe

| Nome | RM |
|------|-----|
| Luis Perrone | RM 369271 |
| Tiago Lopes | RM 369151 |
| João Pires | RM 369186 |
| Karina Felix | RM 369763 |
| Rodrigo Raiche | RM 367254 |

## 💬 Contribuições

Contribuições são bem-vindas! Para contribuir:

1. Fork o projeto
2. Crie uma branch para sua feature (`git checkout -b feature/NovaFeature`)
3. Commit suas mudanças (`git commit -m 'Adiciona nova feature'`)
4. Push para a branch (`git push origin feature/NovaFeature`)
5. Abra um Pull Request

## 📧 Contato

Para questões sobre o projeto, entre em contato através de:
- Issues do GitHub

## 📄 Licença

**MIT License** - Código aberto para fins educacionais e de pesquisa.

Os dados originais estão sujeitos aos termos de uso do IBGE.

---

**Nota:** Este estudo tem caráter acadêmico e exploratório. Para questões relacionadas à violência sexual ou depressão, procure ajuda profissional especializada.

**Recursos de Apoio:**
- CVV - Centro de Valorização da Vida: 188 (24h)
- Disque 180 - Central de Atendimento à Mulher
- Ligue 190 - Polícia Militar (emergências)
