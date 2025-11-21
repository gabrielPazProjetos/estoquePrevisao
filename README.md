--- Previsão de Estoque Inteligente com AWS SageMaker Canvas
-- Objetivo
Este projeto tem como finalidade demonstrar o uso do Amazon SageMaker Canvas para prever a quantidade de estoque de produtos a partir de variáveis como preço, promoção, produto e data.
O Canvas permite criar modelos de machine learning sem necessidade de programação, tornando o processo acessível e eficiente.

--- Dataset escolhido ( Disponivel no repositorio do desafio/aula)
Arquivo: dataset/dataset-1000-com-preco-promocional-e-renovacao-estoque.csv

--- Colunas disponíveis:
- ID_PRODUTO: identificador único do produto
- DATA_EVENTO: data do registro
- PRECO: preço do produto no evento
- FLAG_PROMOCAO: indicador binário de promoção (0 = não, 1 = sim)
- QUANTIDADE_ESTOQUE: quantidade em estoque no evento

--- Passo a Passo no SageMaker Canvas
- Entrar o Amazon SageMaker Canvas pelo console AWS.
- Criar um novo projeto e realizar o upload do dataset CSV.
- Definir QUANTIDADE_ESTOQUE como variável alvo.
- Selecionar como features: ID_PRODUTO, DATA_EVENTO, PRECO, FLAG_PROMOCAO.
- Configurar DATA_EVENTO como variável temporal para enriquecimento automático.
- Executar o treinamento automático (AutoML). 
- Revisar métricas de desempenho e importância das variáveis.
- Exportar previsões para análise e documentação.

--- Resultados
- Promoções reduzem o estoque de forma acelerada.
- Preços mais altos tendem a manter maior quantidade em estoque.
- Efeitos temporais (dia da semana, ciclo do mês) influenciam a demanda. 
- O modelo apresentou métricas adequadas para uso em apoio à decisão de reposição e precificação.

--- Reports
- conclusoes.txt: principais conclusões do modelo.
- modelo_config.txt: configuração utilizada no Canvas.
- previsoes_exemplo.csv: exemplos de previsões exportadas.
- metricas.txt: descrição textual das métricas do modelo.
- insights.txt: insights de negócio derivados das previsões.

--- Requisitos
-- Dependências mínimas para manipulação do dataset:
- pandas
- numpy

--- Limitações
- O modelo depende da qualidade e abrangência do dataset.
- As métricas foram avaliadas qualitativamente, sem valores numéricos exatos.
- Os dados utilizados são fictícios e não representam informações reais (obtidos no repositorio do professor).

Conselhos
- Automatizar a atualização do dataset e o re-treinamento periódico.
- Incluir variáveis adicionais como demanda histórica e tempo de reposição.
- Definir thresholds de estoque mínimo por produto.
- Integrar previsões ao fluxo operacional da empresa.
