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

Após criar o conjunto, você será redirecionado para a página _(Home /Organizations / (sua organização) / (seu conjunto de dados) / Edit / Add New Resource)_.

Selecione o arquivo em sua máquina e clique no botão 'Carregar' (_Load_): 
	
**tela add new resource**
![image](https://user-images.githubusercontent.com/52294411/235779150-0a846533-bb46-4ae3-9d59-e5bda9520b8c.png)

O nome do arquivo deve ser em letras minúsculas, sem espaços, separado por traços '-', sem caracteres especiais, acentos ou letras maiúsculas (nome legível por máquina). Após clicar em load (carregar), o CKAN irá preencher o campo 'nome' automaticamente como o nome do arquivo que for carregado por você.
	
Além disso, o CKAN vai inferir as colunas do arquivo tabular e carregar as informações sobre os metadados de cada uma, para que você preencha:

**tela inferência metadados**
![image](https://user-images.githubusercontent.com/52294411/235779423-197e18e0-89fe-41be-9fc6-90298e3971fe.png)

Note que o nome do cabeçalho de cada coluna aparece, tal qual está registrado no arquivo carregado. Os nomes das colunas (ou cabeçalhos/headers devem ser preferencialmente legíveis por máquina). Também há uma visualização prévia dos valores de cada coluna, ao clicar em _Preview item_, abaixo do nome:

**tela preview item**
![image](https://user-images.githubusercontent.com/52294411/235265080-a4f80f6c-dcae-4ea8-95e7-6cb4f2438213.png)
	
Cada caixa pertence a uma coluna, que deve ter, pelo menos Título (_Title_), Descrição (_Description_), Tipo (_Type_) e Formato (_Format_). Clique em Editar metadado (_Edit Metadata_) para editar os metadados de cada coluna:

**tela inferência metadados coluna**
![image](https://user-images.githubusercontent.com/52294411/235264994-53357788-1dc7-4977-b4d3-050fd0773e9c.png)
	
O título e a descrição devem ser legíveis por pessoas, então comportam acentos, espaços, maiúsculas, caracteres especiais.

O tipo e o formato dos valores de cada coluna são inferidos automaticamente pelo CKAN, mas você pode alterá-los, se julgar que um outro representa melhor o dado de determinada coluna. 

Mais detalhes sobre as especificações de tipos e formatos de coluna nas [Especificações da _Frictionless Data_('dados sem fricção')](https://specs.frictionlessdata.io/table-schema/#field-descriptors).

Você pode ampliar a qualidade da documentação dos teus dados, adicionando propriedades:

- requerido (_required_), se for obrigatório ter dados na coluna (não pode haver campo 'NULL');
- valores únicos (_unique_), se todos os valores da coluna forem únicos;
- chaves primária (_Primary Key_) e/ou estrangeira (_Foreign Key_), para indicar variáveis (coluna) que conectam tabelas (modelo entidade-relacionamento/M.E.R.)
- extras (clicar no botão '+ Add Metadata'):
	- max/min (valores mínimo e máximo, se numeral)
	- pattern (expressão regular, com sintaxe definida no [XML Schema regular expression syntax](http://www.w3.org/TR/xmlschema-2/#regexs))
	- enum (lista exaustiva que indica todos os possíveis valores de uma coluna)

**tela Add Metadata**
![image](https://user-images.githubusercontent.com/52294411/235783577-3291d706-8633-4d3c-9d5d-0a248761fc7f.png)

Mais informações sobre a aplicabilidade de cada metadado restritivo (_constraints_) em [_Frictionless Table Schema Fields Constraints_](https://specs.frictionlessdata.io/table-schema/#constraints.

Para qualquer arquivo (recurso ou _Resource Data_) incluído, também são necessários título (_Title_) e descrição (_Description_). Além disso, o formato (_Format_), tipo (_type_) e _encoding_ também são obrigatórios, mas já vêm inferidos pelo CKAN.

**tela metadados recurso**
![image](https://user-images.githubusercontent.com/52294411/235780576-6b0c758c-9261-4776-b29d-7a62a5f66e04.png)

Você também pode adicionar mais metadados do recurso, clicando no botão '+Add Metadata'

**tela add metadata**

Se o conjunto contiver somente um recurso, clique no botão '_Validate_', para checar o resultado na porção superior da página. Aparecendo o texto em verde '_Successfully saved resourse_', pode clicar no botão 'Publish', no canto inferior da página (o botão '_PUBLISH_' fica esmaecido, e somente se torna acessível, num tom azul-escuro, após você clicar em '_Validate_'). 

![image](https://user-images.githubusercontent.com/52294411/235782539-3d554c36-f931-4398-983c-40e732691441.png)

![image](https://user-images.githubusercontent.com/52294411/235782711-44bca63d-11f7-4423-8bb4-1867c5ec6a08.png)

![image](https://user-images.githubusercontent.com/52294411/235782829-d41e5233-374b-4732-9e32-09bce15844e0.png)
	
**OBS.IMPORTANTE!** o texto que aparece após clicar no botão 'Validate' não corresponde ao resultado da checagem se os dados estão de acordo com os metadados informados, mas somente que o processo aconteceu. O resultado fica numa '_badge_' (ou etiqueta) de validação na página inicial de cada conjunto, com os dizeres _DATAPACKAGE VALID_ (válido) ou _DATAPACKAGE INVALID_ (inválido).


## Adicionar mais recursos e editar metadados

Para adicionar mais um recurso, clique no botão '+ Add Resource' no final da página:

**tela add resource**
![image](https://user-images.githubusercontent.com/52294411/235264889-294a182e-4328-4b56-bc47-ef6b0d6ead0b.png)
	
Se você já tiver publicado um conjunto apenas com o primeiro recurso, pode voltar a adicionar mais recursos, após clicar no conjunto, e no botão Gerenciar (_Manage_). Então, na tela abaixo, clicar em '+Add new resource':

**tela add new resource pos publish**
![image](https://user-images.githubusercontent.com/52294411/235785430-e49fe674-331f-4275-90f6-4b358078a302.png)
	
## Incluir um relacionamento (chaves primária '_primary Key_'e estrangeira '_foreign Key_')

Serve para representar o relacionamento entre colunas com mesmos valores (instâncias) de duas tabelas (recursos) que dizem respeito a um mesmo fenômeno. A visualização das referências entre as colunas que se relacionam podem ser notadas nas setas [deste conjunto-teste](http://projetockan.cge.mg.gov.br/datapackage-creator/show-diagram/teste-rapido-sprint-6). As chaves são incluídas nas caixas de adição de metadados, como as telas a seguir mostram:

**primary Key**
![image](https://github.com/Andrelamor/manual-abertura-2023-3/assets/52294411/55fbbabc-9863-463f-832b-18363ddcd911)

**foreign Key**
![image](https://github.com/Andrelamor/manual-abertura-2023-3/assets/52294411/bd8c622a-6e68-4eca-9fef-680a34a893c2)

