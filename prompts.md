# Prompts reutilizáveis — Miniguia IA aplicada à Análise de Dados

Este arquivo reúne prompts testados e prontos para usar no NotebookLM. Use os placeholders entre colchetes e substitua por nomes de arquivos, trechos, variáveis ou objetivos específicos.

## 1. Resumos
- Prompt resumo executivo (curto):
  "Leia o arquivo [NOME_DO_ARQUIVO] e escreva um resumo executivo de 150–200 palavras destacando 5 conceitos-chave e 3 aplicações práticas. Cite a seção ou página quando possível."

- Prompt resumo estruturado (tópicos):
  "Resuma o arquivo [NOME] em 5 tópicos: (1) problema, (2) metodologia, (3) resultados, (4) limitações, (5) recomendações. Cada tópico com 2–4 bullets. Cite fontes/trechos."

- Prompt para extrair passos/receita:
  "A partir do arquivo [NOME] liste um passo a passo replicável para montar um pipeline de análise de dados, incluindo pré-processamento, seleção de features, modelo sugerido e métricas de avaliação. Formato: lista numerada."

## 2. Flashcards e Revisão Ativa
- Gerar flashcards:
  "Gere 10 flashcards do arquivo [NOME], formato: Pergunta — Resposta curta (1–2 linhas). Numere-os."

- Perguntas de múltipla escolha:
  "Crie 8 questões de múltipla escolha sobre [TEMA], cada uma com 4 alternativas e indique a resposta correta com uma breve justificativa (máx. 1 frase)."

## 3. Diagnóstico e Melhoria de Modelos
- Diagnóstico de desempenho:
  "Com base na descrição do modelo em [ARQUIVO/TRECHO], liste 6 possíveis causas para desempenho insatisfatório e proponha 1 ação corretiva priorizada para cada causa."

- Checklist de boas práticas:
  "Gere um checklist com 12 itens para revisar antes de colocar um modelo em produção (ex.: validação, monitoramento, testes de regressão, explainability)."

## 4. Prompts Técnicos (pipelines, feature engineering, validação)
- Pipeline recomendado:
  "Descreva um pipeline detalhado para um problema de previsão de [TARGET] com dados tabulares: etapas, transformações, técnicas de feature engineering, algoritmos sugeridos e estratégia de validação. Limite: 8 passos claros."

- Engenharia de features:
  "Com base no arquivo [NOME] proponha 6 features novas (descrição + razão) e indique possíveis riscos (correlação espúria, leakage)."

## 5. Prompts para Evitar Alucinações e Forçar Citações
- Estrito, com fonte obrigatória:
  "Responda somente com fatos verificados nas fontes fornecidas. Para cada afirmação, cite a fonte e a página/seção. Se a informação não estiver nas fontes, responda: 'não encontrado nas fontes'."

- Usando trechos como contexto:
  "Utilizando apenas os trechos abaixo (entre três aspas), responda à pergunta X e cite exatamente a linha/parte do trecho usada: '''[COLE O TRECHO AQUI]'''. Pergunta: [SUA PERGUNTA]."

## 6. Formatos de Saída (controle de estilo)
- Formato em bullets curtos:
  "Formato: 5 bullets numerados. Cada bullet com no máximo 20 palavras."

- Tabela resumida:
  "Gere uma tabela com colunas: Conceito | Definição curta | Aplicação prática | Fonte. Máximo 8 linhas."

## 7. Variações e Cicatrizes (exemplos de troubleshooting)
- Problema: respostas genéricas -> variação: adicionar 'Use apenas o arquivo [NOME] como referência'.
- Problema: falta de citações -> variação: adicionar 'Inclua referência: seção/página/linha'.
- Problema: saída muito longa -> variação: 'Responda em no máximo 120 palavras'.

## 8. Exemplo prático (prompt + resultado esperado)
Prompt:
"Leia o capítulo 3 do arquivo statlearning_ch3.pdf e resuma em 5 bullets os métodos apresentados, indicando a página de cada método."
Resultado esperado (exemplo):
1. Método A — descrição curta. (p.45)
2. Método B — descrição curta. (p.48)
... 

---
Dicas finais:
- Sempre comece pedindo o formato desejado (bullets, tabela, flashcards).
- Quando possível, forneça trechos do documento para reduzir o risco de alucinações.
- Salve no NotebookLM as versões que deram melhor resultado para poder reutilizar/afinar posteriormente.
