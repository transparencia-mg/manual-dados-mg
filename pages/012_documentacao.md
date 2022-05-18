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

- utilizando a linha de comando: 

[apresentação para oficina SEJUSP](https://github.com/dados-mg/apresentacoes/blob/master/hands-on/SEJUSP-hands-on-2022-04-12.pptx), ocorrida em 14/04/2022;

[apresentação para oficina SEPLAG](https://github.com/dados-mg/apresentacoes/blob/master/hands-on/SEPLAG-hands-on-2022-03-30.pptx), ocorrida em 30/03/2022



[^] Definição de metadados obrigatórios e facultativos

* referência da [publicação da FGV](https://www.gov.br/cgu/pt-br/governo-aberto/a-ogp/planos-de-acao/4o-plano-de-acao-brasileiro/compromisso-2-docs/modelo-de-referencia-de-abertura-de-dados_versao-final-2.pdf), a partir das pp. 28-30: 

> Com base na Recomendação Boas Práticas para Dados na Web (DWBP)44, sugerimos que os metadados a seguir sejam obrigatórios:

• Título;
• URI;
• Palavras-chave;
• Data da publicação;
• Publicador;
• Autoria;
• Ponto de contato (e-mail e/ou telefone); ==> incluir como orientação??
• Período da publicação;

- licença (orientação para aplicação da Creative Commons Atribuição - resolução ou norma?)

- procedência ==> incluir como orientação??

- versão e histórico (propriedade obrigatória datapackage.json; funcionalidade CKAN e controle versão GITHUB)