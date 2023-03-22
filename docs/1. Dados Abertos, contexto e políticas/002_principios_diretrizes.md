# Princípios e Diretrizes

**[Leis dos Dados Abertos](https://eaves.ca/2009/09/30/three-law-of-open-government-data/) - por David Eaves:**

São proposições amplamente difundidas sobre as características mínimas esperadas para uma base aberta de dados. Gestores governamentais e publicadores devem cuidar para que essas características estejam asseguradas, de modo a promover o acesso, uso e reuso dos dados.

1. Se o dado não pode ser encontrado e indexado na web, ele não existe. 


    bases de dados de datawarehouses ou sistemas internos de acesso restrito não são abertos  
  
2. Se não estiver aberto e disponível em formato compreensível por máquina, ele não pode ser reaproveitado. 
 
    
    arquivos não-estruturados, como boletins (em pdf) não são compreendiddos por programas

3. Se algum dispositivo legal não permitir sua reaplicação, ele não é útil.


    dado disponível na web, em formato aberto e estruturado, mas tem uma licença restringindo seu uso

**Formatos**

Conforme a [Cartilha Técnica para Publicação de Dados Abertos no Brasil](https://wiki-dados-h.cgu.gov.br/GetFile.aspx?Page=Tecnologia&File=Cartilha%20T%c3%a9cnica%20para%20Publica%c3%a7%c3%a3o%20de%20Dados%20Abertos%20no%20Brasil%20v1.pdf), os principais formatos de dados abertos são os arquivos com as seguintes extensões:

  .csv, .xml, .ods, .rdf, .json

Os formatos de dados mais utilizados no Portal de Dados Abertos de Minas Gerais são:

- o `csv`, para os dados

- o `json`, para os metadados;

Ambos têm uma característica essencial, que é ser **tabular**.

**Representação do dado tabular**:

````
campo     campo
  |         |
  |         |
  V         V

 A     |    B    |    C    |    D      <--- linha (cabeçalho)
 ------------------------------------
 valA  |   valB  |  valC   |   valD    <--- linha
````
 
 **csv**:

 - Um bom exemplo de definição, características e exemplos do dado em formato `.csv` encontra-se no [portal de Dados Abertos de Buenos Aires](https://datosgcba.github.io/guia-datos/guia-abiertos/#csv)
 
 - como editar, importar e exportar, pode ser melhor verificado em: https://rockcontent.com/br/blog/csv/


**json**:

````
[
  { "A": valor, "B": valor, ... },
  { "A": valor, "B": valor, ... },
  ...
]
````

* Uma caracterização desse formato tabular com as especificações utilizadas no Portal de Dados Abertos pode ser encontrada em: https://specs.frictionlessdata.io/table-schema/#concepts

**O dialect: como fazer representar o arquivo de dados `.csv`:**

Parte dos metadados são formas de representação lógica dos próprios dados (tal qual um mapa visa descrever um território). Uma informação de metadado necessária para correta leitura, interpretação e reuso dos dados tabulares em formato `.csv` é a sua descrição lógica num arquivo `dialect.json`. Um exemplo dessa descrição lógica, da estrutura do arquivo csv:

````
{
  "dialect": {
    "delimiter": ";",
    "doubleQuote": true,
    "lineTerminator": "\r\n",
    "quoteChar": "\"",
    "skipInitialSpace": true,
    "header": true,
  }
}

````

Os formatos `.PDF, .DOC, .DOCX, .XLS e .XLSX` são INCOMPATÍVEIS com a filosofia dos dados abertos!


**Escala de Dados Abertos**

Uma figura comum nas cartilhas e materiais que trata de fazer mostrar o grau de maturidade dos dados de acordo com um conjunto de atributos necessários, prescritos nas leis e normas (incluindo até a terceira estrela abaixo)e desejáveis

★ : dados disponíveis na web (não importa o formato) sob uma licença aberta. Por exemplo, um PDF.

★ ★ : dados disponíveis de forma estruturada. Por exemplo, excel no lugar de imagem escaneada.

★ ★ ★ : dados disponíveis em formatos não-proprietários. Por exemplo, um CSV e não excel.

★ ★★ ★: identificador uniforme de recurso (exemplo?) 

★ ★★ ★★ : dados conectados (exemplo?) RDF/LOD

![image](https://user-images.githubusercontent.com/52294411/226441191-1dfef786-da09-4f82-ad94-de6fc5e7ba7c.png)

Nessa escala, o dado é considerado efetivamente aberto quando alcança o nível de três estrelas.

As demais estrelas fornecem mais possibilidades, como navegar mais facilmente por eles e encontrar novas informações e relações.

## Aplicação dos pricípios e normativos no Portal de Dados Abertos de MG/PdA:

| princípio                              | referência legal                              | arquitetura PdA                                                                                                                                                                                                                  |
|----------------------------------------|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| oportuno, atual                        | Lei 12527, art. 8 § 3º, VI             | frequência de atualização equivalente à das consultas do Portal da   Transparência; versionamento em repositório com controle e informação da   periodicidade de atualização como propriedade de metadado no datapackage.json |
| compreensível                          | Lei 12527, art. 8 § 3º, IV             | adoção de dicionário de dados com padrão predefinido                                                                                                                                                                          |
| acessível                              | Lei 12527, art. 8 § 3º, III            | disponibilização dos datasets na plataforma CKAN, com possibilidade de   requisições via API                                                                                                                                  |
| utilizável, processável por máquina                             | Lei 12527, art. 8 § 3º, II             | formatos abertos e estruturados dos arquivos de recursos dos datasets   (csv, json)                                                                                                                                           |
| comparável                             | Decreto Federal 8777/2016: art. 2º, IV | especificação documentada publicamente através dos datapackage.json                                                                                                                                                           |
| interoperável | Lei 12527, art. 8 § 3º, III            | adoção do padrão Frictionless Data                                                                                                                                                                                            |

## Saiba Mais

Conheça mais um pouco sobre a importância dos dados abertos, suas diferenças e complementaridades com o Portal da Transparência no [17º episódio do PodeFalar!](https://www.youtube.com/watch?v=uFdYbIc_4ws), o nosso podcast da CGE, em que a então Subcontroladora de Transparência e Integridade, Nicolle Bleme, conversou com a Diretora-Executiva da Open Knowledge Brasil, Fernanda Campagnucci.

