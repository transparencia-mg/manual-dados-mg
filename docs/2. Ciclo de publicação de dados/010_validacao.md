---
comments: true
tags:
  - publicação
  - validação
  - metadados
  - qualidade
---

# Validação Automática 

Esta etapa também serve para para oferecer informação íntegra aos usuários. Consiste em comparar se os dados de cada variável espelham fielmente a descrição contida no respectivo dicionário de dados. 

## Verificar a validação dos dados no Portal de Dados com o plugin ckanext-datapackage-creator

**tela 1ª validação com um recurso**
![image](https://user-images.githubusercontent.com/52294411/235264375-c3aae20c-e3fa-49f7-943a-32b6369b908d.png)

Para cada edição em algum recurso em que o botão 'Publish' tenha sido acionado, haverá um novo relatório de validação acessível, como exemplificado abaixo:

![image](https://user-images.githubusercontent.com/52294411/235788319-564166d7-ca89-403b-a473-f4255eb4f165.png)
No caso acima, houve uma referência incorreta de chaves primária (primary key) e chave estrangeira (foreign key). 

#### Corrigir eventuais inconsistências (rol exemplificativo)

1. Tipo de dado da coluna: data, numeral inteiro/decimal, com vírgulas, etc
2. Chaves primária e estrangeira

3. Nomes cabeçalho 
4. Linhas repetidas
5. Encoding

## Verificar relacionamento

**tela DER com 1º recurso**
![image](https://user-images.githubusercontent.com/52294411/235264314-ce96eb4a-b268-4b6e-ab10-ca9002f66f95.png)
**tela DER com um chaveamento/relação entre 2 tabelas**
![image](https://user-images.githubusercontent.com/52294411/235786800-3c4c4ad8-b703-44c5-b0df-e001160aaf20.png)

## Verificar dicionários de dados

**tela dicionário de dados**
![image](https://user-images.githubusercontent.com/52294411/235264281-eb229f34-7f0a-400c-9be0-99a1da899cde.png)

**tela view metadata**
![image](https://user-images.githubusercontent.com/52294411/235264263-c21ab52f-eede-4e4e-9a69-9d75ae3b0b1f.png)


## Operação da validação com o framework da Frictionless Data

O conjunto de ferramentas da especificação Frictionless permite automatizar a validação, seja no HD local, ou conectado a um repositório github onde o conjuntos de dados esteja hospedado.

Na **oficina "Dados abertos sem fricção" ([vídeo](https://www.youtube.com/watch?v=tZ0bmlnqMuY) e [apresentação](https://ead.prodemge.gov.br/pluginfile.php/19736/mod_resource/content/2/Dados%20Abertos%20sem%20friccao-DCTA-CGE.pdf))** realizada em novembro de 2020, durante a semana INOVA, foi demonstrado como preparar um conjunto de dados para publicação, com ferramenta online da _Frictionless Data_ (especificação de metadados utilizada no Portal de Dados Abertos). Seu conteúdo inclui a documentação de um pequeno conjunto de dados, com a ferramenta online [_datapackage creator_](https://create.frictionlessdata.io/) seguido da validação e limpeza.

O **webnário "Como gerenciar dados abertos utilizando o DPCKAN" ([vídeo](https://www.youtube.com/watch?v=oTCQX5a9eXY) e [apresentação](https://transparencia-mg.github.io/reveal.js/presentations/20230328_gerenciar_dados_abertos_com_dpckan/index.html))**, realizado na Escola de Dados da Open Knowledge Brasil, em março de 2023, também abordou exemplos de como inferir, documentar os metadados e validá-los, com a ferramenta CLI (linha de comando) dpckan e também com a extensão (plugin) ckanext-datapackage-creator, de interface gráfica (GUI).

Uma lista compreensiva dos erros de validação mais comuns pode ser acessada na próxima sessão.

