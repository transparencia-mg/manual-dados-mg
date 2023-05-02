---
comments: true
tags:
  - publicação
  - capacitação
  - tutoriais
  - guias
  - treinamento
---

# Oficinas, capacitações, palestras, webnarios

[webnario OKBr março/2023 - Gerenciando dados no CKAN com dpckan e ckanext-datapackage-creator](https://transparencia-mg.github.io/reveal.js/presentations/20230328_gerenciar_dados_abertos_com_dpckan/index.html)

# roteiro oficina

![image](https://user-images.githubusercontent.com/52294411/235708922-ea9682a8-5f30-41c9-b611-d1a5a6e5b9a9.png)

## intro (4 slides - máx. 10min)


![image](https://user-images.githubusercontent.com/52294411/235719411-25869bc6-010b-4b93-864c-299df02a150a.png)

- - - 
1
![image](https://user-images.githubusercontent.com/52294411/235705786-b506164d-08d3-40ba-aec2-e1cc85d51607.png)


- - - 
2
![image](https://user-images.githubusercontent.com/52294411/235702265-7da1c054-1d92-485f-b4ea-89279cec4057.png)

https://github.com/ckan/ckan


- - - 
3
![image](https://user-images.githubusercontent.com/52294411/235703452-f20606ed-3db3-45cb-9248-3fc779d5a0c4.png)

https://ckan.org/blog/the-ckan-30-team-is-formed-welcome-to-dragan-and-svetozar


- - - 
4
![image](https://user-images.githubusercontent.com/52294411/235704328-972bc2b7-bae7-43f2-aa09-31a6dd5f2378.png)

## fluxo publicação (1 slide + mão-na-massa - 50min)


- - -
5
- login - http://projetockan.cge.mg.gov.br/organization/oficina-semana-mineira-de-controle

- navegação básica (menu superior e lateral)

- adicionar conjunto (30 nomes diferentes por turma - pensar na estratégia - sugestão é distribuir número por mesa para identificar, ex.: conjunto-teste-oficina-1, conjunto-teste-oficina-2)

	- níveis de agregação: recursos > conjunto

	- metadados obrigatórios do conjunto

		- nome legível por máquina

		- título legível em português

		- descrição

		- profile (datapackage ou package), segundo Frictionless Data

		- URL

		- organização (sugestão: criar uma organização específica para a oficina http://projetockan.cge.mg.gov.br/organization/oficina-semana-mineira-de-controle)

		- contatos do publicador/mantenedor

		- licença

		- frequência de atualização
		
		- palavras-chave
		- versão

- adicionar recurso

	- escolher arquivos salvos (link repo github: https://github.com/transparencia-mg/termos-parceria-contratos-gestao/tree/main/data)

	- metadados obrigatórios do recurso

		- nome legível por máquina

		- título legível em português

		- descrição

		- formato arquivo (inferido automaticamente pela ferramenta)

		- encoding arquivo (inferido automaticamente - recomendação forte de uso do utf-8, para leitura e parsemanto/interpretação por ferramentas de dados como pacotes do R e do python)

	- metadados obrigatórios das colunas (explicar o por que disso - dicionários de dados legíveis por pessoas e por máquina/json gerados automaticamente permitirão a interpretação do conteúdo sintático dos dados; na primeira vez, parece ser mais repetitivo e toma um trabalho a mais, mas com potenciais benefícios para auxiliar os usuários, que inclui colegas da adm, ou outros poderes, e tb reduzir demandas repetidas - foco na garantia de um padrão de qualidade, interpretação adequada e aumento da possibilidade de uso do dado)

		- nome legível por máquina

		- título legível em português

		- descrição

		- tipo

		- formato

		- adicionais (chaves primária e estrangeira; )

		- restrições (extensão, para strings; mínimo e máximo, para numerais; lista)

- verificar validação

	- identificar os erros

	- corrigir um erro de tipo de coluna

- inserir relacionamento entre tabelas

	- metadados de chave primária e estrangeira

	- verificar diagrama de entidade-relacionamento

	- simular e corrigir erro de relacionamento

- publicar dados

- visualizar dicionários de dados

	- legível por pessoa

	- legível por máquina: datapackage.json

	- (confirmar alcance de baixar e manipular dados com ferramentas CLI a partir do API show) 

- - - 

## considerações (2 slides)

- em qual patamar estamos na escala de qualidade dos dados 

![image](https://user-images.githubusercontent.com/52294411/235706596-7d9b1db7-26e7-4d8e-afa1-1b89a3e561e6.png)

- - - 

- sobre atendimento aos requisitos legais:

![image](https://user-images.githubusercontent.com/52294411/235706961-51f46cf8-9c15-46b9-9be0-a50cead198c2.png)
https://andrelamor.github.io/manual-abertura-2023-3/0.1/1.%20Dados%20Abertos%2C%20contexto%20e%20pol%C3%ADticas/001_normas_legais/

- o plugin ainda é matéria de testes, e a oficina também serve para captar dúvidas e necessidades de ajustes

- a oficina ficará gravada para consulta e prática

- também temos uma versão em elaboração do Manual de Dados Abertos, para consulta e aberta para observações e sugestões

- prevemos subir esse ambiente que vamos usar para o PdA em julho (?), juntamente com a agregação de dúvidas e observaçoes no Manual

## tira-dúvidas (30min)
