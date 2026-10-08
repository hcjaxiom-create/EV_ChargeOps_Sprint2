# EV ChargeOps - Sprint 2

## Descrição

O EV ChargeOps é um protótipo desenvolvido para gerenciamento inteligente de sessões de recarga de veículos elétricos em infraestruturas compartilhadas.

A solução registra sessões de recarga, calcula consumo individual, realiza o rateio de custos, gera indicadores operacionais e utiliza Inteligência Artificial para detectar anomalias e prever consumo.

## Funcionalidades implementadas

- Registro de sessões de recarga
- Organização dos dados por usuário e unidade
- Cálculo de consumo individual
- Cálculo do custo de cada sessão
- Rateio por usuário
- Indicadores operacionais
- Gráficos de consumo e custo
- Detecção simples de consumo fora do padrão
- Detecção de anomalias com Isolation Forest
- Classificação de risco
- Recomendações automáticas para o gestor
- Previsão de consumo utilizando Regressão Linear
- Avaliação do modelo com MAE, MSE, RMSE e R²
- Exportação dos resultados para CSV

## Inteligência Artificial

A IA possui função estrutural dentro do protótipo.

O módulo de Inteligência Artificial utiliza:

### Isolation Forest

Utilizado para detectar sessões de recarga com comportamento anômalo considerando consumo de energia e duração da sessão.

### Regressão Linear

Utilizada para estimar o consumo esperado de energia com base na duração da sessão.

Os resultados são utilizados para apoiar a classificação de risco e a tomada de decisão do gestor.

## Tecnologias utilizadas

- Python
- Google Colab
- Pandas
- NumPy
- Matplotlib
- Scikit-learn

## Arquivos principais

- `EV_ChargeOps_Sprint2.ipynb` - notebook principal com o protótipo funcional
- `ev_chargeops_resultados.csv` - dados processados e resultados das análises
- `README.md` - documentação do projeto

## Como executar

1. Abra o arquivo `EV_ChargeOps_Sprint2.ipynb` no Google Colab.
2. Execute as células na ordem apresentada.
3. Também é possível utilizar a opção "Ambiente de execução > Executar tudo".
4. Analise os resultados, gráficos, indicadores e classificações geradas.

## Decisões técnicas

O desenvolvimento foi realizado em Google Colab para facilitar a execução, demonstração e validação do protótipo.

Os dados utilizados nesta Sprint são simulados, permitindo validar a lógica central da solução antes de uma futura integração com dados reais do carregador GoodWe HCA G2.

A escolha do Isolation Forest permite identificar comportamentos fora do padrão sem necessidade de uma base previamente rotulada.

A Regressão Linear foi utilizada como modelo simples de previsão por ser de fácil interpretação e adequada ao objetivo de demonstrar o funcionamento da camada preditiva.

## Desvios em relação à Sprint 1

A arquitetura inicialmente proposta previa uma aplicação utilizando Streamlit e SQLite.

Durante a Sprint 2, foi adotado um notebook executável em Google Colab como protótipo funcional, permitindo concentrar a validação da lógica de negócio, do rateio, dos indicadores e dos módulos de Inteligência Artificial.

A mudança mantém os objetivos funcionais definidos na Sprint 1 e facilita a demonstração técnica da solução.

## Evidências de funcionamento

As evidências do protótipo estão disponíveis no notebook e nas imagens abaixo:

- `01_painel_gestor.png` - painel consolidado com sessões, consumo, custo e alertas.
- `02_ia_anomalias.png` - resultado do módulo de IA com classificação de sessões normais e anômalas.
- `03_previsao_consumo.png` - gráfico comparando consumo real e consumo previsto.

Além das imagens, o arquivo `EV_ChargeOps_Sprint2.ipynb` contém todas as células executadas, tabelas, métricas, gráficos e resultados do protótipo.

## Possíveis melhorias

- Integração com dados reais do carregador GoodWe
- Interface web em Streamlit
- Banco de dados em nuvem
- Autenticação de usuários
- Dashboards em tempo real
- Histórico de cobrança
- Alertas automáticos
- Modelos preditivos mais avançados

## Autor

Hugo Camisotti Junior
