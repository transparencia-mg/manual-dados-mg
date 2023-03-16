# Princípios e Diretrizes

**[Leis dos Dados Abertos](https://eaves.ca/2009/09/30/three-law-of-open-government-data/) - por David Eaves:**

1. Se o dado não pode ser encontrado e indexado na web, ele não existe. 


    bases de dados de datawarehouses ou sistemas internos de acesso restrito não são abertos  
  
2. Se não estiver aberto e disponível em formato compreensível por máquina, ele não pode ser reaproveitado. 
 
    
    arquivos não-estruturados, como boletins (em pdf) não são compreendiddos por programas

3. Se algum dispositivo legal não permitir sua reaplicação, ele não é útil.


    dado disponível na web, em formato aberto e estruturado, mas tem uma licença restringindo seu uso

**Formatos**

Conforme a Cartilha Técnica para Publicação de Dados Abertos no Brasil, os principais formatos de dados abertos são os arquivos com as seguintes extensões:

  .csv, .xml, .ods, .rdf, .json


Os formatos `.PDF, .DOC, .DOCX, .XLS e .XLSX` são INCOMPATÍVEIS com a filosofia dos dados abertos!

**Escala de Dados Abertos**

★ : dados disponíveis na web (não importa o formato) sob uma licença aberta. Por exemplo, um PDF.

★ ★ : dados disponíveis de forma estruturada. Por exemplo, excel no lugar de imagem escaneada.

★ ★ ★ : dados disponíveis em formatos não-proprietários. Por exemplo, um CSV e não excel.

★ ★★ ★: identificador uniforme de recurso (exemplo?) RDF

★ ★★ ★★ : dados conectados (exemplo?) LOD

![escala](https://user-images.githubusercontent.com/52294411/225652134-886dff90-f20b-4925-948b-552039901a63.png)

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

Clique [aqui](http://www.transparencia.mg.gov.br/) e conheça o Portal da Transparência do Estado de Minas Gerais.
