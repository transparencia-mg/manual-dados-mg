# Validação Automática 

Esta etapa também serve para para oferecer informação íntegra aos usuários.

Consiste em comparar se os dados de cada variável espelham fielmente a descrição contida no respectivo dicionário de dados. 

O conjunto de ferramentas da especificação Frictionless permite automatizar a validação, seja no HD local, ou conectado a um repositório github onde o conjuntos de dados esteja hospedado:

[](!static/dados-validos.png)

Uma lista compreensiva dos erros de validação mais comuns pode ser acessada [aqui](https://github.com/dados-mg/dados-mg.github.io/blob/erros-valiacao/erros-validacao/erros-comuns-validacao.md), da qual um resumo pode ser visto abaixo:

1. Sintaxe do `datapackage.json`:

- faltou fechar algum campo com ']' ou '}'
- faltou/sobrou alguma vírgula

2. Nome (`name`) do recurso contém caracteres fora das especificações permitidas

3. O caminho (`path`) incorreto:

- onde se localizam os arquivos de dados
- onde se localizam os arquivos de metadados `datapackage.json`, o `schema.json`, ou o `dialect.json`


4. Divergências de características dos dados no `datapackage.json`

- número decimal/porcentagem (string X number)
- formatos de data
- dado obrigatório ausente
- valor fora da faixa

5. Arquivo de dados sem encoding `utf-8` 

6. Datapackage sem a propriedade `owner-org` obrigatória

## Operação da validação com o framework da Frictionless Data