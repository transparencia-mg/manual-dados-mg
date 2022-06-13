# Documentação

A documentação se destina a descrever as características básicas do conjunto de dados (nome, título, descrição, tipo, variáveis, padrões de valores, licença, autor, organização, etc). O produto final esperado é a elaboração de um arquivo de metadados.

Pelo padrão de dados sem fricção _frictionless_ adotado para o Portal de Dados Abertos de Minas Gerais, essas características têm valores e formatos próprios, predeterminados, para serem utilizados no arquivo de metadados. Tais características visam permitir a fácil acessibilidade, interpretabilidade e reuso dos dados.

A adoção do padrão _frictionless_ permite o uso de ferramentas que facilitam a execução dessa etapa de documentação, ou descrição, dos dados. São as ferramentas usuais para esse trabalho: 

- o [datapackage creator](https://create.frictionlessdata.io/): ferramenta online, de interface gráfica, para descrição manual dos campos de metadados que representarão as características dos dados, em seus 3 níveis, que compõem um _datapackage_ (colunas/variáveis, arquivos/recursos e conjunto/dataset)

![](static/datapackage-creator.png)

- [_frictionless describe_](https://framework.frictionlessdata.io/docs/guides/describing-data/): instrução a ser repassada na linha de comando (bash cell/CLI), que infere os metadados básicos de um determinado arquivo de dados (após instalação e configuração - vide [^] setup da máquina )  


## Criação de um datapackage com o framework da Frictionless Data

- utilizando a ferramenta online:

A oficina "Dados abertos sem fricção" ([vídeo](https://www.youtube.com/watch?v=tZ0bmlnqMuY) e [apresentação](https://ead.prodemge.gov.br/pluginfile.php/19736/mod_resource/content/2/Dados%20Abertos%20sem%20friccao-DCTA-CGE.pdf)) contém uma demonstração de como preparar um conjunto de dados para publicação. Seu conteúdo inclui a documentação de um pequeno conjunto de dados, com a ferramenta online _datapackage creator_ seguido da validação e limpeza.

Uma outra referência, textual, para uso do _datapackage creator_, pode ser encontrada no [blog da _frictionless data_](https://frictionlessdata.io/blog/2019/05/20/used-and-useful-data/#include-a-data-schema)

- utilizando a linha de comando: 

[apresentação para oficina SEJUSP](https://github.com/dados-mg/apresentacoes/blob/master/hands-on/SEJUSP-hands-on-2022-04-12.pptx), ocorrida em 14/04/2022;

[apresentação para oficina SEPLAG](https://github.com/dados-mg/apresentacoes/blob/master/hands-on/SEPLAG-hands-on-2022-03-30.pptx), ocorrida em 30/03/2022


## Metadados obrigatórios e facultativos no Portal de Dados Abertos de Minas Gerais

#### Obrigatórios

Conjunto (_dataset_):

 - Perfil (_profile_): para identificar a tipologia do conjunto de acordo com a especificação Dados sem Fricção (_frictinoless data_)

 - Nome (_name_): legível por máquina, sem espaços ou caracteres especiais

 - Título (_title_): legível por pessoas

 - Descrição (_description_): _"Como Participar"_, "_Controle de Alterações_"

 - Catálogo origem (_homepage_): Página (URL) do órgão onde está publicado o conjunto de dados.

 - Organização (_owner_org_): Entidade custodiante dos dados 

 - Versão (_version_): indica a versão do conjunto; também deve estar discriminada e detalhada na seção `CHANGELOG`

 - Publicador (_title_, _role_ e _mail_): nome, papel e e-mail de contato do setor responsável pela autoria e publicação dos dados

 - Licença (_name_, _title_ e _path_): para garantir o reúso indiscriminado dos dados abertos, com a devida atribuição da fonte

 - Palavras-chave/etiquetas (_keywords_)

 - Frequência de Atualização dos dados: intervalo temporal de atualização dos dados

Recursos (_resources_):

 - Perfil (_profile_): para identificar a tipologia do recurso de acordo com a especificação Dados sem Fricção (_frictinoless data_)

 - Nome (_name_): legível por máquina, sem espaços ou caracteres especiais

 - Título (_title_): legível por pessoas

 - Descrição (_description_):

 - Formato (_format_) do arquivo

 - Codificação (_encoding_) do arquivo

 - Pasta de localização do arquivo (_path_)

 - Dicionário de dados (_schema_): características de cada variável (coluna, se tabular)

 	- Nome (_name_)

 	- Título (_title_)

 	- Tipo (_type_)

 	- Formato (_format_)

 	- Descrição (_description_)

#### Facultativos

 - Documentação: URL de documento que expõe detalhes sobre o conjunto de dados.

 - Cobertura geográfica: Localização ou região geográfica a que se referem os dados. Ex.: Recife.

 - Cobertura temporal: Data ou período à que referem os dados. Ex.: 03/2012.

 - Granularidade geográfica: Precisão geográfica da cobertura geográfica. Ex.: municipal.

 - Granularidade temporal: Precisão temporal da cobertura temporal. Ex.: mês.

 - Referências: Relações com outros conjuntos de dados.

 - Metodologia: Processo de criação dos dados.

 - Vocabulário/ontologia: Documentos estruturados com metadados específicos do conjunto de dados.


* [portal federal](https://dados.gov.br/pagina/padrao-de-metadados) - metadados obrigatórios e desejáveis (conciliar com ckan, frictionless e Transparência Internacional):


* referência da [publicação da FGV](https://www.gov.br/cgu/pt-br/governo-aberto/a-ogp/planos-de-acao/4o-plano-de-acao-brasileiro/compromisso-2-docs/modelo-de-referencia-de-abertura-de-dados_versao-final-2.pdf), a partir das pp. 28-30: 

