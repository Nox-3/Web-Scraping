# Web Scraper de Produtos

Este script Python é um web scraper que busca informações de produtos de um site específico e foi desenvolvido via Google Colab .

## Dependências

O script depende das seguintes bibliotecas Python:

- os
- requests
- BeautifulSoup

## Como usar

1. Insira o link do site na variável `url_base`.
2. O arquivo `DscProduto.txt` deve conter as consultas de produtos a serem pesquisadas.
3. O script irá criar um arquivo `resultados.txt` que contém os resultados da pesquisa.
4. As consultas já processadas serão salvas no arquivo `consultas_ja_realizadas.txt`.
5. Se ocorrer um erro de codificação durante a consulta, a consulta será salva no arquivo `consultas-erro-codificacao.txt`.

## Funcionamento

O script lê cada consulta do arquivo de entrada. Para cada consulta, ele faz uma solicitação GET para a URL do produto e extrai o título e o preço do produto usando BeautifulSoup. Ele limita os resultados a 3 por consulta(Sendo possivel alterar o limite).

Se a consulta já foi processada (ou seja, está presente no arquivo `consultas_ja_realizadas.txt`), a consulta é ignorada.

Se ocorrer um erro de decodificação durante a consulta, a consulta é salva no arquivo `consultas-erro-codificacao.txt` e a próxima consulta é processada.

Os resultados da pesquisa são salvos no arquivo `resultados.txt`.

## Nota

Este script foi criado para fins educacionais e não deve ser usado para scraping em sites sem permissão.
