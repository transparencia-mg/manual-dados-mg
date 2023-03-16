---
comments: true
tags:
  - publicação
---
# Limpeza de Dados

Esta etapa tem o objetivo de oferecer informação íntegra aos usuários. A limpeza não se constitui, necessariamente, uma primeira etapa de uma sequência ordenada de ações. Ela usualmente é necessária após a documentação, ou validação dos dados, na medida em que forem identificadas incorreções, incompletudes ou inadequações com os metadados descritos. 

Exemplos: padronização do formato de valores de colunas (siglas, números, datas, unidades de medida); inclusão ou exclusão de colunas para padronização do layout dos arquivos.

Na figura a seguir, temos algumas inadequações na planilha de remuneração:

- Falta de padrão para valores:

    - na 2ª coluna: Valor abreviado 'SD 1 CL' e outros por extenso;

    - na 3ª coluna: zero ('0'), vazios ('') e 'sim';

    - na 5ª coluna: valor 'CBMMG' (nome do órgão abreviado) e outros nomes por extenso;

    - na 7ª coluna: separadores de milhar e de decimais para remuneração
    
- Formatos de número a serem descritos para valores de carga horária, na 6ª coluna; 

- Formato de descrição da data (última coluna): necessidade de descrição no datapackage.json (como %d%m%a)

![limpeza-exemplo](https://user-images.githubusercontent.com/52294411/225653960-5fc2c8d3-f0ed-4d4d-850a-8514f812b17c.png)

A responsabilidade pela limpeza dos dados deve ser da área produtora (ou custodiante). Um guia sugestivo de problemas comuns de limpeza de dados responsável, pode ser encontrado [na EScola de Dados da Open Knowledge Brasil](https://escoladedados.org/tutoriais/guia-quartz-para-limpeza-de-dados/).

O guia divide o tipo de problema pelo responsável indicado para resolvê-lo, como, por exemplo:

* problemas que a fonte dos dados deve resolver: faltam valores, linhas duplicadas, formatos de datas inconsistentes, unidades de medida não estão especificadas, categorias estão mal escolhidas, origem não está documentada, nomes de campos estão ambíguos, texto foi convertido em números, números foram guardados como texto;

* problemas que o usuário dos dados deve resolver: dados foram editados manualmente, escala de tempo foi manipulada, inflação distorce os dados, amostra não é aleatória, amostra é enviesada, margem de erro é muito grande, margem de erro é desconhecida, 

