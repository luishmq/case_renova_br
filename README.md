# Case Técnico Renova BR 🔎📚
Foi requisitado a análise e tratamento de dados oriundos do repositório de dados eleitorais do TSE (Tribunal Superior Eleitoral). Esses dados representam as eleições municipais de São Paulo do ano de 2020.

![]()

# 1.0 Descrição dos dados

## 1.1 Dados referentes ao perfil do eleitorado

| Atributos                          | Descrição                                                                                                                                             |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| DT_GERACAO                             | Data da extração dos dados |
| HH_GERACAO | Horário da extração dos dados |
| ANO_ELEICAO | Ano da eleição |
| SG_UF | Sigla da unidade da federação do eleitor |
| CD_MUNICIPIO | Código do município |
| NM_MUNICIPIO | Nome do município |
| CD_MUN_SIT_BIOMETRIA | Código da situação biométrica do município  |
| DS_MUN_SIT_BIOMETRIA                     | Descrição da situação biométrica do município |
| NR_ZONA | Número da zona eleitoral |
| CD_GENERO | Código do gênero |
| DS_GENERO | Descrição do gênero |
| CD_ESTADO_CIVIL | Código do estado civil |
| DS_ESTADO_CIVIL | Descrição do estado civil |
| CD_FAIXA_ETARIA                            | Código da faixa etária do eleitor |
| DS_FAIXA_ETARIA | Descrição da faixa etária do eleitor |
| CD_GRAU_ESCOLARIDADE | Código do grau de escolaridade do eleitor |
| DS_GRAU_ESCOLARIDADE | Descrição do grau de escolaridade do eleitor |
| QT_ELEITORES_PERFIL | Quantidade de eleitores aptos |
| QT_ELEITORES_BIOMETRIA                            | Quantidade de eleitores aptos, com biometria cadastrada |
| QT_ELEITORES_DEFICIENCIA | Quantidade de eleitores aptos com biometria deficiência ou mobilidade reduzida  |
| QT_ELEITORES_INC_NM_SOCIAL | Quantidade de eleitores aptos que solicitaram inclusão do nome social |

## 1.2 Dados referentes aos resultados eleitorais

| Atributos                          | Descrição                                                                                                                                             |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| DT_GERACAO                             | Unique identifier for each store |
| HH_GERACAO | Date on which the sale event occurred |
| ANO_ELEICAO | Numeric variable that represents the day of the week |
| CD_TIPO_ELEICAO | Day's sales value |
| NM_TIPO_ELEICAO | Number of customers in the store on the day |
| CD_PLEITO | Indicator for store open = 1 or closed = 0 |
| DT_PLEITO | Indicates whether the day is a state holiday. a = Public holiday, b = Easter holiday, c = Christmas, 0 = No holiday |
| NR_TURNO                     | Indicates whether or not the store was closed during the school holiday |
| store_type | Indicates the model of stores. Can vary between a, b, c, d |
| assortment | Indicates the level of product variety: a = basic, b = extra, c = extended |
| competition_distance | Distance (in metres) to nearest competitor |
| competition_open_since [Month/Year] | Indicates the year and month in which the nearest competitor opened |
| promo | Indicates if the store has an active promotion on the day | 
| promo_2                            | Indicates whether the store continued the promotion: 0 = store not participating, 1 = store participating |
| promo_2_since [Year/Week] | Describes the year and week when the store starts the extended promotion |
| promo_interval | Describes the months in which the store started the promo2. For example, "Feb,May,Aug,Nov" means that the store started the extended promotions in each of these months |

# 2.0 Estratégia de solução

# 3.0 Tratamento de Dados

# 4.0 Filtragem de Dados

# 5.0 Join e Insights
