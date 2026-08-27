# Miniguia: Inteligência Artificial aplicada à Análise de Dados — NotebookLM

> Caderno temático preparado para o desafio DIO: construir um Caderno Temático com NotebookLM documentando curadoria, engenharia de prompts e um miniguia final sobre IA aplicada à Análise de Dados.

## 1. Contexto e Objetivos
- Tema escolhido: Inteligência Artificial aplicada à Análise de Dados — fundamentos, ferramentas e boas práticas.
- Objetivos de estudo:
  - Entender os conceitos fundamentais de IA e como aplicá-los em pipelines de análise de dados.
  - Conhecer ferramentas práticas (pandas, scikit-learn, TensorFlow/PyTorch, notebooks) e boas práticas de engenharia de dados e modelagem.
  - Documentar e testar prompts no NotebookLM para gerar resumos, flashcards e guias reutilizáveis.
  - Consolidar resultados em um miniguia final com resumos, glossário e prompts reutilizáveis.

## 2. Curadoria de Fontes (3–5)
As fontes abaixo foram selecionadas como referência e sugeridas para upload no NotebookLM. Substitua pelos PDFs/arquivos que você efetivamente carregar no NotebookLM quando necessário.

1. "An Introduction to Statistical Learning" — Gareth James et al. (PDF gratuito)
   https://www.statlearning.com/
2. "Python Data Science Handbook" — Jake VanderPlas (Capítulos online / Jupyter)
   https://jakevdp.github.io/PythonDataScienceHandbook/
3. scikit-learn — User Guide e tutoriais
   https://scikit-learn.org/stable/tutorial/index.html
4. "Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow" — Aurélien Géron (exemplos)
   https://github.com/ageron/handson-ml2
5. Guia de Feature Engineering (curso/coleção de artigos)
   https://www.kaggle.com/learn/feature-engineering

(Indique aqui os nomes dos arquivos que você subiu no NotebookLM, ex.: statlearning_ch3.pdf, python_data_science_ch1.ipynb, scikit_tutorial.pdf)

## 3. Engenharia de Prompts e "Cicatrizes"
Registro das perguntas estratégicas, variações testadas, resultados e problemas.

- Prompt base — resumo de arquivo:
  "Resuma em até 300 palavras os principais pontos do arquivo [NOME_DO_ARQUIVO], destacando 5 conceitos-chave, 3 aplicações práticas e referencie o trecho/página usado."

- Variações testadas:
  - "Gere um resumo executivo (150–200 palavras) e uma lista de 5 bullets com ações práticas para aplicar este conteúdo em um projeto de análise de dados."
  - "Liste os passos para construir um pipeline reproducível baseado nas técnicas deste arquivo, incluindo transformações, validação e métricas recomendadas."
  - "Crie 10 flashcards (pergunta/resposta) cobrindo os conceitos essenciais deste material."

- Cicatrizes (problemas encontrados) e soluções:
  - Problema: respostas sem indicação de onde a informação veio (sem citações).
    Solução: incluir no prompt "Cite a seção/página do arquivo correspondente; se não houver, escreva 'não encontrado nas fontes'".
  - Problema: respostas genéricas (não específicas ao arquivo).
    Solução: fornecer trecho/trechos relevantes como contexto no input e pedir "usando apenas os trechos fornecidos".
  - Problema: alucinações (fatos não presentes nas fontes).
    Solução: prompt estrito: "Responda apenas com informações explicitamente presentes nas fontes fornecidas.".
  - Problema: saída muito longa ou mal estruturada.
    Solução: pedir formato rígido (ex.: "Formato: 5 bullets numerados; cada bullet com máximo 20 palavras").

- Registro de interações (exemplo de log):
  - Prompt: "Resuma capítulo 2 em 5 bullets e cite a página."
    Resultado: (cole a resposta obtida do NotebookLM + indicação de qual fonte/arquivo foi usada).
  - (Repita para 3–5 prompts com notas sobre qualidade e ajustes feitos.)

## 4. Miniguia de Estudo (Entrega Final)

4.1 Resumo executivo (exemplo)
A aplicação de Inteligência Artificial à análise de dados integra etapas de preparação de dados, seleção/engenharia de features, modelagem e avaliação. Ferramentas como pandas e scikit-learn são essenciais para pipelines clássicos; frameworks como TensorFlow ou PyTorch são recomendados para modelos mais complexos. Boas práticas incluem: limpeza e versionamento de dados, validação cruzada adequada, tratamento de viés/variáveis confusoras, automação de pipelines e documentação reprodutível. (150–200 palavras)

4.2 Resumos por tópico (exemplo de subtópicos)
- Preparação de dados: limpeza, imputação, tratamento de outliers, transformação e normalização.
- Engenharia de features: criação, seleção, codificação categórica, redução de dimensionalidade.
- Modelagem: escolhas de algoritmos (regressão, árvores, ensemble, redes neurais), tuning de hiperparâmetros.
- Avaliação: métricas (RMSE, AUC, F1, precisão/recall), validação cruzada, divisão treino/validação/teste.
- Deploy e monitoramento: versionamento de modelos, testes de desempenho em produção, detecção de drift.

4.3 Glossário (principais conceitos)
- Inteligência Artificial (IA): campo que estuda sistemas que exibem comportamento inteligente.
- Aprendizado de Máquina (ML): subcampo da IA que constrói modelos a partir de dados.
- Feature / Atributo: variável usada pelo modelo.
- Engenharia de Features: processo de criar e transformar features para melhorar modelos.
- Pipeline: sequência automatizada de etapas de processamento e modelagem.
- Cross-Validation: técnica para avaliar generalização do modelo.
- Overfitting: ajuste excessivo aos dados de treino.
- Underfitting: modelo incapaz de capturar padrões dos dados.
- Hyperparameter Tuning: busca pelos melhores parâmetros do modelo.
- Data Drift: mudança nas distribuições de dados ao longo do tempo.

4.4 Conjunto de prompts reutilizáveis (em português)
- Resumo curto por arquivo:
  "Leia o arquivo [NOME] e resuma os 5 pontos mais importantes em 5 bullets; cite seção/página."
- Gerar flashcards:
  "Gere 10 flashcards do conteúdo de [ARQUIVO], formato: Pergunta — Resposta curta."
- Recomendação de pipeline:
  "Com base em [ARQUIVO/TRECHO], descreva um pipeline passo a passo para analisar um dataset com target [VARIÁVEL], incluindo transformações, modelo sugerido e métrica de avaliação."
- Diagnóstico de modelo:
  "Liste possíveis causas de desempenho ruim para o modelo descrito em [ARQUIVO] e proponha 5 ações corretivas priorizadas."
- Preparar exercício prático:
  "Crie 3 exercícios práticos com enunciado e solução breve para treinar o conceito X do arquivo [NOME]."

## 5. Plano de Estudo / Cronograma (exemplo)
- Semana 1: coleta e upload das 3 fontes principais no NotebookLM; leitura e prompts iniciais (resumos).
- Semana 2: engenharia de prompts, geração de flashcards e criação de resumos por tópico.
- Semana 3: elaboração do miniguia final, montagem do glossário e preparação da entrega DIO.

## 6. Evidências / Anexos
- Incluir prints / trechos de interações com o NotebookLM (cole aqui as respostas relevantes).
- Lista de arquivos carregados no NotebookLM: ex.: statlearning_ch3.pdf, python_data_science_handbook_ch4.pdf, scikit_tutorial_notes.pdf.
- Exemplo de interação colada (prompt + resposta) como prova de trabalho.

## 7. Como entregar na DIO (passo a passo)
1. Crie um repositório no GitHub e cole este README.md com seu conteúdo finalizado.
2. Copie a URL do repositório.
3. No desafio DIO, clique em "Entregar projeto", cole o link e escreva uma breve descrição (ex.: "Miniguia: IA aplicada à Análise de Dados — resumos, glossário e prompts com NotebookLM").
4. Confirme a entrega.

## 8. Observações finais e sugestões de nome de repositório
Sugestões:
- miniguia-ia-analise-dados
- ia-analise-dados-notebooklm
- caderno-ia-analise-dados

Boa prática: torne o repositório público para facilitar a avaliação e o portfólio (a menos que seus arquivos contenham dados sensíveis).
