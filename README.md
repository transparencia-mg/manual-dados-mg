# Manual de Abertura de Dados

Manual para Abertura de dados criado pela Diretoria de Transparência Ativa - DTA com auxílio de gerador de site estático [Livemark](https://frictionlessdata.github.io/livemark-project), [Docker](https://hub.docker.com/repository/docker/gabrielbdornas/livemark), [GitHub Actions](https://github.com/features/actions) e [Github Pages](https://pages.github.com/).


## Estrutura para construção do Manual

O gerador de site estático livemark, a partir do comando [`build`](https://livemark.frictionlessdata.io/pages/getting-started/building-website.html#build) transforma arquivos `markdown` em `html`. Por definição deste repositório, todos estes arquivos, `markdown` criados e `html` gerados, deverão ser armazenados na pasta `pages`.
Exceção à esta regra são os arquivos `index.md` e `index.html`, localizado na raiz do repositório. Estes são responsáveis pela geração da página inicial deste Manual.
O arquivo `livemark.yaml` é responsável, entre outras coisas, por criar o menu lateral esquerdo do site. 
Sendo assim, o mesmo deverá ser alimentado sempre que um novo arquivo `markdown` seja criado.

Um erro comum durante a construção utilizando a biblioteca `livemark` é criar arquivos `markdown`, incluí-lo no arquivo `livemark.yaml` e deixá-lo em branco. 
Todo arquivo `markdown` deverá ter, no mínimo, um `#` para evitar erros durante processo de `build`.

## Makefile

O arquivo `Makefile`, presente na raiz repositório, é responsável por:
	
- Automatizar o processo de `build`, tanto via Github Actions quanto localmente;
- Criar servidor local para teste, sendo com isso possível acessar o conteúdo criado via navegador no endereço `http://localhost:7000/`.

Para listar todos os comandos criados no arquivo `Makefile`, bem como uma breve descrição dos mesmos basta digitar `make` no terminal

```Terminal
$ make
```
## Build e visualização local utilizando Makefile e Docker

Utilizando Docker é possível ativar ambiente com todos os pacotes necessários para `build` via comando `make container`.
Este iniciará Docker Container aonde será possível executar os comandos, principais, `make build` e `make start`

## Build e visualização local utilizando ambiente virtual python e Makefile

Obs.: Devido a um [problema](https://github.com/frictionlessdata/livemark/issues/205) para realização do `build` em sistema operacional Windows, sugerimos utilizar esta opção apenas em Linux ou MacOS.

Caso usuário deseje utilizar comandos Makefile sem a utilização do Docker, será necessário utilizar ambiente virtual python com a ferramenta livemark instalada:

```Teminal
# Criação, ativação de ambiente python e instalação de pacotes - Windows
$ python -m venv venv
$ source venv/Scripts/activate
$ pip install livemark

# Criação, ativação de ambiente python e instalação de pacotes - Linux
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install livemark
```

Como ambiente ativado e pacotes instalados será possível executar os comandos, principais, make build e make start.