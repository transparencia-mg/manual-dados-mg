---
comments: true
tags:
  - publicação
  - capacitação
  - tutoriais
  - guias
  - treinamento
---
- [Apresentação sobre dados abertos](https://github.com/dados-mg/dados-mg.github.io/blob/invitation/dados-abertos-pcmg-2023-02-16.pptx?raw=true)

- Material estático com o ambiente de treinamento versão CKAN produção 2.10 + plugin ckanext-datapackage-creator

- Vídeo/tutorial do treinamento (link da Gravação da capacitação/oficina hands-on da Semana do Controle Interno de maio de 2023 a ser incluído após oficina do dia 10/05)  

# Publicando dados no Portal de Dados Abertos de MG

## Login

Acesse sua conta inserindo login de usuário e senha. Para isso, você precisa solicitar a criação do teu usuário, instruções em [Solicitação de Cadastro de Novo Usuário no Portal de Dados Abertos]():

![image](https://user-images.githubusercontent.com/52294411/235250208-db525f1c-cf73-4896-9740-eb75f1c0a76c.png)

## Criar e documentar novo conjunto de dados

Após fazer login, na página de [Conjuntos de Dados(Datasets)](), clicar no botão azul 'Adicionar Conjunto de Dados':

**tela add dataset**

Após clicar no botão de criação, na página 'Criar um conjunto de dados (Create dataset)', preencha as informações básicas (metadados) do conjunto a ser criado:

- título (_Title_)
- descrição (_Description_)
- selecione a organização (_Organization_) responsável pelos dados a serem publicados (já foi cadastrada previamente pelo administrador do sistema na DCTA/CGE)
- selecione a visibilidade (_Visibility_) do conjunto: pública (_Public_) ou restrita para usuário logado (_Private_) (por padrão/default, a seleção vem marcada como '_private_')  
- selecione o tipo dos dados do conjunto(_Type_): tabular ou não-tabular(_Not Tabular_)
- seleciona a licença(_License_), dentre as opções que o CKAN oferece para licenças abertas 

![image](https://user-images.githubusercontent.com/52294411/235251657-9cd82ace-e26b-43e8-9bf4-3c055c20bfc7.png)

Ainda na mesma página 'Criar um conjunto de dados (Create dataset)':

- Preencha uma página/site/URL (_Source_), caso haja, com a fonte original da base de dados, ou uma página informativa sobre a base ou sobre o setor responsável pela publicação

- Informe a versão (_Version_) corrente do conjunto a ser publicado (dicas para atribuição de versão em **inserir link**)

- Contribuidores (_Contributors_): o publicador (_Publisher_) já vem preenchido automaticamente com as informações de nome do login e email; caso o autor (_Author_) da base seja diferente do publicador (alguém de outro setor, por exemplo, informar nos campos correspondentes. Também é possível informar um site/URL referente ao publicador ou autor (**inserir exemplo**).

- Você também pode adicionar um 'Contribuidor', após clicar em '+Add Contributor' e selecionar seu tipo (_Select the contributor type_). A documentação do CKAN permite vários tipos, mas sugerimos restringir aos tipos publicador (_Publisher_), autor (_Author_) ou mantenedor (_Maintainer_)

- Selecione a Frequência de Atualização (_Frequency_) na lista correspondente:
  - Diária (_Daily_)
  - Semanal (_Weekly_)
  - Bi-semanal (_Fortnightly_)
  - Mensal (_Monthly_)
  - Bimestral (_By-monthly_)
  - Trimestral (_Quarterly_)
  - Anual (_Annual_)
  - Por evento (_On Demand_)

- Insira palavras-chave no campo 'Etiquetas', separando-as por vírgulas e espaço, para facilitar a identificação, classificação, filtragem/seleção e acesso ao seu conjunto de dados (o campo livre, mas sugere-se o reaproveitamento de vocabulários controlados e analogias a legislações da área temática e com outros portais de dados **inserir link para VCGE federal**)

![image](https://user-images.githubusercontent.com/52294411/235250980-859fe8b1-f8e1-46d0-b4aa-dc60be6c2f4e.png)

* OBS.: os metadados Título (_Title_), Descrição (_Description_) e Organização (_Organization_) são obrigatórios, por isso estão marcados com asterisco

* os metadados Licença (_License_) e Publicador (_Publisher_) são requisitos para um conjunto ser considerado aberto por suas características intrínsecas de acesso livre e de facilidade de acesso/contato com o responsável

* Frequência de Atualização (_Frequency_) também é um metadado muito importante e fortemente recomnedado, para assegurar uma regularidade e fixar uma expectativa concreta quando às novas atualizações e inserção de novos dados e/ou recursos

* Dica: verifique a página onde você está navegando no menu superior da página (Home / Conjunto de Dados / Criar um conjunto de dados >>)


## Adicionar recurso

## Documentar os metadados do recurso

## Verificar a validação dos dados

#### Corrigir eventuais inconsistências (rol exemplificativo)

1. Tipo de dado da coluna: data, numeral inteiro/decimal, com vírgulas, etc
2. Encoding
3. 

## Verificar relacionamento

## Verificar dicionários de dados

## Publicar dados

## Baixar conjunto de dados
