---
comments: true
tags:
  - publicação
  - metadados
  - qualidade
---
# Documentação: Elaboração e edição dos Metadados

## Necessidade e Diretrizes

Na escala de maturidade de dados sugerida pela [Sunlight Foundation](https://sunlightfoundation.com/2019/08/15/an-open-data-maturity-scale-for-cities-to-find-right-sized-solutions/), reduzir barreiras para acessar informações é considerada a intervenção mais básica na abertura de dados. Uma das formas de reduzir barreiras é prover um esquema de metadados. A LAI representou essa diretriz em seu artigo 8º.  

Um esquema de metadados visa permitir a contextualização dos campos dos conjuntos dos dados. Em outras palavras, evidenciar a qualificação e usos dos mesmos, como por exemplo: quando ficou publicamente acessível; a data da última atualização; se é derivada de uma fonte primária, ou se foi modificada; qual sua licença de uso.

Trata-se, enfim, de informação que descreve, explica, localiza ou torna mais fácil de usar, manejar ou recuperar um dado. Quanto mais informação sobre o dado estiver provida de forma padronizada, mais valioso tal dado se torna.

Ter metadados, em um catálogo de todas as bases de dados (abertos ou não) foi um dos quesitos avaliados na [Escala Brasil Transparente da CGU](http://transparencia.gov.br/pdf/bfe87072-8531-4dcc-9a9d-d6aefab0c1b7.pdf#catalogo-ou-inventario-de-dados-abertos). Os atributos dos metadados requeridos nessa metodologia de avaliação foram: descrição do conteúdo, periodicidade de atualização, origem e responsável pelo gerenciamento, tamanho e formato.

A W3C, entidade internacional que desenvolve padrões para a web, elaborou um [Guia de Melhores Práticas](https://www.w3.org/TR/dwbp/#metadata), em que existem três itens relacionados a metadados:

1. Fornecer metadados ([BP1](http://blog.w3c.br/melhores-praticas-dados-na-web-2-forneca-metadados-umapordia/)) para leitura de pessoas e máquinas (computadores). Para leitura humana, poderia ser [parte de uma página HTML na web](https://www.w3.org/TR/dwbp/dwbp-example.html) ou um arquivo de texto em separado. Para leitura por máquina, os metadadaos poderiam ser providos em formato JSON, ou [embutidos no formato HTML](https://www.w3.org/TR/dwbp/dwbp-example.ttl) - sob a recomendação de reutilizar padrões de vocabulários populares.


2. Fornecer metadados descritivos ([BP2](http://blog.w3c.br/melhores-praticas-dados-na-web-3-forneca-metadados-com-parametros-de-localidade/)), de forma que pessoas entendam a natureza do conjunto de dados e suas distribuições (i.e. título, descrição, palavras-chave, data de publicação, entidade responsável pela publicação e contato com a mesma, cobertura temporal e espacial, data da última modificação e categorias) e agentes de software descobrirão automaticamente tais conjuntos e distribuições.


3. Fornecer metadados estruturais ([BP3](http://blog.w3c.br/melhores-praticas-dados-na-web-4-forneca-metadados-com-informacoes-estruturais/)), de forma que pessoas interpretem o esquema de um conjunto de dados e agentes de software sejam capazes de processar automaticamente os dados das distribuições

Os metadados devem, por fim, permitir a interoperabilidade entre diferentes sistemas. 


## Metadados no Portal de Dados Abertos de Minas Gerais

Os conjuntos de dados (_datasets_) do Portal de Dados Abertos de Minas Gerais estão documentados conforme as especificações Frictionless Data (dados sem fricção), que atendem à caracterização descrita acima e possibilitam a validação automática dos dados por serviços ofertados pela comunidade.

Os padrões de epecificação da _Fricitonless Data_ utilizam o formato `json` para descrição de metadados, e acompanham um conjunto de ferramentas de código aberto (bibliotecas, aplicações e instruções em diferentes linguagens) para aplicar os 
padrões. Dessa maneira, facilitam a gestão de metadados, a extração, a documentação, a limpeza, a organização, a validação e o compartilhamento dos dados. 

Documentação é a etapa de elaborar os documentos de metadados de um conjunto de dados, enquanto que a validação corresponde à verificação se os dados estão de acordo com os metadados descritos.

Estas etapas poderiam ser custosas (i.e. tempo e esforço) demais para publicadores de dados, não fosse a possibilidade de emprego de ferramentas de código aberto, que permitem a automatização de boa parte desse trabalho.

Os padrões de especificação Frictionless podem ser consultados [aqui](https://specs.frictionlessdata.io/tabular-data-package/#language)

## Datapackage (pacote de dados)

Segundo a especificação _frictionless data_ (Dados sem Fricção) adotada para o Portal de Dados Abertos, as propriedades das variáveis, dos arquivos (recursos) e do conjunto de dados (dataset) devem estar descritas num formato padronizado e legível por máquina.

A junção dos arquivos de dados, com os arquivos contendo a descrição (metadados) dessas três instâncias (variáveis, recrursos e conjunto) formam um `datapackage`

![datapackage](https://user-images.githubusercontent.com/52294411/225654987-97fd5518-f04b-4aec-8196-ae80d80db229.png)

A maior parte dos conjuntos têm sido descrita num formato tabular, com o arquivo separado por vírgulas (ou ponto-e-vírgula), extensão `.csv`, que pode ser representado assim:

![tabular](https://user-images.githubusercontent.com/52294411/225655081-78c447af-d0e1-469a-b924-5fa75ba9252f.png)

As propriedades desse tipo de arquivo tabular (_tabular data resource_) estão descritas na [especificação _frictionless data_](https://specs.frictionlessdata.io/tabular-data-resource/#specification).

Já para cada variável, ou coluna, a _frictionless_ sugere um _table schema_, cuja especificação pode ser encontrada [aqui](https://specs.frictionlessdata.io/table-schema/). Pode-se elencar um conjunto mínimo de propriedades dessas variáveis/colunas:

* Nome (legível por máquina, sem letras maiúsculas, sem acentos, espaços ou caracteres especiais);

* Formato da variável (_string, number, boolean, date_, etc)

* Título (humanamente legível)

* Descrição (humanamente legível)

Não obstante, são exatamente essas 4 propriedades básicas que constam do Dicionário de Dados do Portal de Dados Abertos, conforme exemplo abaixo (coluna = nome, tipo = formato, rótulo = título):

![dicionario](https://user-images.githubusercontent.com/52294411/225655187-91f96aaa-913e-4830-b58c-8feefe5440d4.png)

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

 ![](assets/images/dataset-json.png)

Recursos (_resources_):

 - Perfil (_profile_): para identificar a tipologia do recurso de acordo com a especificação Dados sem Fricção (_frictinoless data_)

 - Nome (_name_): legível por máquina, sem espaços ou caracteres especiais

 - Título (_title_): legível por pessoas

 - Descrição (_description_):

 - Formato (_format_) do arquivo

 - Codificação (_encoding_) do arquivo

 - Pasta de localização do arquivo (_path_)

![resource-json](https://user-images.githubusercontent.com/52294411/225655500-e24e5f85-f89c-4c2b-bb55-dc8e9534f8a7.png)

 - Dicionário de dados (_schema_): características de cada variável (coluna, se tabular)

 	- Nome (_name_)

 	- Título (_title_)

 	- Tipo (_type_)

 	- Formato (_format_)

 	- Descrição (_description_)

 ![schema-json](https://user-images.githubusercontent.com/52294411/225655600-538cfbfd-7e79-4bcb-9fcf-eecd64397a89.png)

[^] a ordem das propriedades nos datapackage.json quase nunca é igual; 

	não estamos publicando `description` nos conjuntos do `age7`

#### Facultativos

 - Documentação: URL de documento que expõe detalhes sobre o conjunto de dados.

 - Cobertura geográfica: Localização ou região geográfica a que se referem os dados. Ex.: Recife.

 - Cobertura temporal (_temporal_): Data ou período à que referem os dados. Ex.: 03/2012.

 - Granularidade geográfica: Precisão geográfica da cobertura geográfica. Ex.: municipal.

 - Granularidade temporal: Precisão temporal da cobertura temporal. Ex.: mês.

 - Referências: Relações com outros conjuntos de dados.

 - Metodologia: Processo de criação dos dados.

 - Vocabulário/ontologia: Documentos estruturados com metadados específicos do conjunto de dados.


## Saiba Mais

A oficina "Dados abertos sem fricção" ([vídeo](https://www.youtube.com/watch?v=tZ0bmlnqMuY) e [apresentação](https://ead.prodemge.gov.br/pluginfile.php/19736/mod_resource/content/2/Dados%20Abertos%20sem%20friccao-DCTA-CGE.pdf)), ocorrida durante a 3ª Semana INOVA, apresenta um passo-a-passo de como preparar um conjunto de dados segundo essas especificações, utilizando ferramentas online. Seu conteúdo inclui a demonstração de ferramentas que objetivam reduzir ou eliminar “a fricção”, que é o tempo que os consumidores gastam para poder entender e trabalhar com os dados abertos.

No capítulo sobre [Etapas do Processo de Abertura de Dados](https://transparencia-mg.github.io/manual-abertura/pages/005_documentacao.html), cada parte desse processo é explicado com mais detalhes.
