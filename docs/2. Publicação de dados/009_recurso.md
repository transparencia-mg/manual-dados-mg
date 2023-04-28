---
comments: true
tags:
  - publicação
  - capacitação
  - tutoriais
  - guias
  - treinamento
---

# Adicionar recurso e documentar seus metadados

Após criar o conjunto, você será redirecionado para a página (_Home /Organizations / <sua organização> / <seu conjunto de dados> / Edit / Add New Resource_).

Escolha um nome, em letras minúsculas, separado por traços '-', sem caracteres especiais, espaços, acentos ou letras maiúsculas (nome legível por máquina).

Selecione o arquivo em sua máquina e clique no botão 'Carregar' (_Load_)

**tela add new resource**

O CKAN vai inferir as colunas do arquivo tabular e carregar as informações sobre os metadados de cada uma, para que você preencha:

**tela inferência metadados**

Note que o nome do cabeçalho de cada coluna aparece, e também há uma visualização prévia dos valores de cada coluna, ao cliar em _Preview item_, abaixo do nome:

**tela preview item**

Cada caixa pertence a uma coluna, que deve ter, pelo menos Título (_Title_), Descrição (_Description_), Tipo (_Type_) e Formato (_Format_). Clique em Editar metadado (_Edit Metadata_) para editar os metadados de cada coluna:

**tela inferencia metadados coluna**

O título e a descrição devem ser legíveis por pessoas, então comportam acentos, espaços, maiúsculas, caracteres especiais.

O tipo e o formato dos valores de cada coluna são inferidos automaticamente pelo CKAN, mas você pode alterá-los, se julgar que um outro representa melhor o dado de determinada coluna. 

[referência sobre especificação da Fricionless para type e format]

Você pode ampliar a qualidade da documentação dos teus dados, adicionando propriedades:

- requerido (_required_), se for obrigatório ter dados na coluna;
- valores únicos (_unique_)
- chaves primária (_Primary Key_) e/ou estrangeira (_Foreign Key_)
- extras (clicar no botão '+ Add Metadata'):
	- max/min
	- pattern
	- enum

**tela Add Metadata**

Para qualquer arquivo (recurso ou _Resource Data_) incluído, também são necessários título (_Title_) e descrição (_Description_). Além disso, o formato (_Format_), tipo (_type_) e _encoding_ tamb´´em são obrigatórios, mas já vêm inferidos pelo CKAN

**tela metadados recurso**

Você também pode adicionar mais metadados do recurso, clicando no botão '+Add Metadata'

**tela add metadata**

Se o conjunto contiver somente um recurso, clique no botão 'Validate', para checar o resultado na porção superior da página. Aparecendo o texto em verde '', pode clicar no botão 'Publish', no canto inferior da página. 

OBS.: o texto que aparece após clicar no botão 'Validate' não correspnode ao resultado da checagem se os dados estão de acordo com os metadados informados, mas somente se o processo aconteceu.

Caso queira adicionar mais recursos, veja na subseção seguinte.

## Adicionar mais recursos e editar metadados

Para adicionar mais um recurso, clique no botão '+ Add Resource' no final da página:

**tela add resource**