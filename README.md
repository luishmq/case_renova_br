# Case Técnico Renova BR 🔎📚
Foi requisitado a análise e tratamento de dados oriundos do repositório de dados eleitorais do TSE (Tribunal Superior Eleitoral). Esses dados representam as eleições municipais de São Paulo do ano de 2020.

![](imgs/logo-tse.jpg)

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
| QT_ELEITORES_BIOMETRIA | Quantidade de eleitores aptos, com biometria cadastrada |
| QT_ELEITORES_DEFICIENCIA | Quantidade de eleitores aptos com biometria deficiência ou mobilidade reduzida  |
| QT_ELEITORES_INC_NM_SOCIAL | Quantidade de eleitores aptos que solicitaram inclusão do nome social |

## 1.2 Dados referentes aos resultados eleitorais

| Atributos                          | Descrição                                                                                                                                             |
| :-------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------------------------- |
| DT_GERACAO | Data da extração dos dados |
| HH_GERACAO | Horário da extração dos dados |
| ANO_ELEICAO | Ano da eleição |
| CD_TIPO_ELEICAO | Código do tipo de eleição |
| NM_TIPO_ELEICAO | Nome do tipo da eleição |
| CD_PLEITO | Código do pleito |
| DT_PLEITO | Data do pleito |
| NR_TURNO | Número do turno |
| CD_ELEICAO | Código da eleição |
| DS_ELEICAO | Descrição da eleição |
| SJ_UF | Sigla da unidade da federação do eleitor |
| CD_MUNICIPIO | Código do município |
| NM_MUNICIPIO | Nome do município | 
| NR_ZONA | Número da zona eleitoral |
| NR_SECAO | Número da seção eleitoral |
| NR_LOCAL_VOTACAO | Número do local de votação |
| CD_CARGO_PERGUNTA | Código do cargo do candidato |
| DS_CARGO_PERGUNTA | Descrição do cargo do candidato |
| NR_PARTIDO | Número do partido do candidato |
| SG_PARTIDO | Sigla do partido do candidato |
| NM_PARTIDO | Nome do partido do candidato | 
| DT_BU_RECEBIDO | Data de recebimento do boletim de urna |
| QT_APTOS | Quantidade de eleitores aptos |
| QT_COMPARECIMENTO | Quantidade de eleitores que compareceram ao local de votação |
| QT_ABSTENCOES | Quantidade de abstenções |
| CD_TIPO_URNA | Código do tipo da urna |
| DS_TIPO_URNA | Descrição do tipo da urna |
| CD_TIPO_VOTAVEL | Código do tipo de eleitor votável |
| DS_TIPO_VOTAVEL | Descrição do tipo de eleitor votável | 
| NR_VOTAVEL | Número do candidato votável |
| NM_VOTAVEL | Nome do candidato votável |
| QT_VOTOS | Quantidade de votos |
| NR_URNA_EFETIVADA | Número da urna efetivada |
| CD_CARGA_1_URNA_EFETIVADA | Código da carga 1 da urna efetivada |
| CD_CARGA_2_URNA_EFETIVADA | Código da carga 2 da urna efetivada |
| CD_FLASHCARD_URNA_EFETIVADA | Código do flashcard da urna efetivada |
| DT_CARGA_URNA_EFETIVADA | Data da carga da urna efetivada |
| DS_CARGO_PERGUNTA_SECAO | Descrição do cargo |
| DS_AGREGADAS | Descrição das agregações | 
| DT_ABERTURA | Data de abertura da votação |
| DT_ENCERRAMENTO | Data de encerramento da votação |
| QT_ELEITORES_BIOMETRIA_NH | Quantidade de eleitores que utilizaram a biometria |
| DT_EMISSAO_BU | Data de emissão do boletim de urna | 
| NR_JUNTA_APURADORA | Número da junta apuradora |
| NR_TURMA_APURADORA | Número da turma apuradora |

# 2.0 Estratégia de solução

![](imgs/)

# 3.0 Tratamento de Dados

## 3.1 Dropando colunas desnecessárias para a análise:

- Colunas com categorias únicas são fortes candidatas para a exclusão.
- Colunas que informam códigos também serão fortes candidatas.
- Datas devem ser avaliadas primeiramente.

## 3.2 Checando dados nulos:

- Dados do perfil do eleitorado:

![](imgs/)

- Dados dos resultados:

![](imgs/)

13 linhas na coluna 'nm_votavel' como NaN.
Após a análise no notebook, concluiu-se que a remoção das linhas nulas é válida.
Ademais, existem valores '#NULO#' apenas na coluna 'sg_partido', ou seja, não há registro da sigla do partido em certas linhas do conjunto de dados. Isso pode significar que:

- Erro no registro de dados no banco.
- Não há registro da sigla do partido devido ao tipo de voto, como o voto branco.

Nesse caso, é válido deixar esses campos no conjunto de dados, de modo que haja a representação dos dados brancos para uma possível futura análise.


# 4.0 Filtragem de Dados

- Foi realizado uma filtragem dos dados do perfil do eleitorado para perfis votantes concentrados apenas na região de São Paulo.

![](imgs/)

# 5.0 Join e Insights

Foi realizado o merge entre os dois conjuntos de dados, explorando apenas uma amostra de cada um, devido ao tamanho dos arquivos e incapacidade de processamento da minha máquina. 

## 5.1 Qual candidato foi mais votado em cada município - Top 5:

![](imgs/)

## 5.2 Qual gênero mais votou em cada candidato - Top 5:

![](imgs/)

## 5.3 Qual faixa etária mais votou em cada candidato:

![](imgs/)

## 5.4 Qual classe de grau de escolaridade mais votou em cada candidato

![](imgs/)
