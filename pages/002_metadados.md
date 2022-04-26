# Metadados

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

Os conjuntos de dados (datasets) do Portal de Dados Abertos de Minas Gerais estão documentados conforme as especificações Frictionless Data (dados sem fricção), que atendem à caracterização descrita acima e possibilitam a validação automática dos dados por serviços ofertados pela comunidade.

Os padrões de epecificação da Fricitonless Data utilizam o formato json para descrição de metadados, e acompanham um conjunto de ferramentas de código aberto (bibliotecas, aplicações e instruções em diferentes linguagens) para aplicar os 
padrões. Dessa maneira, facilitam a gestão de metadados, a extração, a documentação, a limpeza, a organização, a validação e o compartilhamento dos dados. 

Documentação é a etapa de elaborar os documentos de metadados de um conjunto de dados, enquanto que a validação corresponde à verificação se os dados estão de acordo com os metadados descritos.

Estas etapas poderiam ser custosas (i.e. tempo e esforço) demais para publicadores de dados, não fosse a possibilidade de emprego de ferramentas de código aberto que permitem a automatização de boa parte desse trabalho.

Os padrões de especificação Frictionless podem ser consultados [aqui]()


## Saiba Mais

A oficina "Dados abertos sem fricção" ([vídeo](https://www.youtube.com/watch?v=tZ0bmlnqMuY) e [apresentação](https://ead.prodemge.gov.br/pluginfile.php/19736/mod_resource/content/2/Dados%20Abertos%20sem%20friccao-DCTA-CGE.pdf)), ocorrida durante a 3ª Semana INOVA, apresenta um passo-a-passo de como preparar um conjunto de dados segundo essas especificações, utilizando ferramentas online. Seu conteúdo inclui a demonstração de ferramentas que objetivam reduzir ou eliminar “a fricção”, que é o tempo que os consumidores gastam para poder entender e trabalhar com os dados abertos.

No capítulo sobre [Etapas do Processo de Abertura de Dados](https://transparencia-mg.github.io/manual-abertura/pages/005_documentacao.html), cada parte desse processo é explicado com mais detalhes.