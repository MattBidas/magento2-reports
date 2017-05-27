# magento2-reports

Alternative solution for the problem with the Date format of Reports on Magento2.

Esta é uma solução alternativa para quem está usando o idioma pt_BR (Português Brasileiro) no Admin e tenta gerar um Relatório.

## Getting Started

Downloading this project in Zip format and uncompress.

Fazer o download ou clonar o projeto

Copy folder Reports in your Magento2 Project , example:

Copiar os arquivos do Módulo para sua pasta do Magento2 no app 
Caminho:  
app/code/<nome de sua distro/vendor>/<pasta modulo>
Exemplo: 
app/code/Override/Reports/..arquivos aqui..


<root_folder>/app/code/MyVendor/ .... paste Reports/ here.
ex.: /var/www/html/app/code/Override/Reports/..

### Prerequisites

#### Magento >= 2.1.5 


### Installing

After copied files and folders in app/code/<myvendor>/ run Magento2 CLI Command :  

Após copiar execute os comandos abaixo :


```
Limpar as pastas var/generation/ e var/di/   (dependency injection)
### sudo rm -rf var/generation/* var/di/*

Atualizar os modulos / arquivos usados pelos módulos
### php -f bin/magento setup:upgrade

Gerar os caminhos dos overrides 
### php -f bin/magento setup:di:compile

After
### php -f bin/magento cache:flush 
And 
### php -f bin/magento cache:clean 
```


## Running the tests

Open Magento2 Admin Panel , Go to Reports and Select Submenu Products and click in Bestsellers 

Abra novamente o Admin ou atualize a página e gere seus relatórios.

Type date initial and date finish (range to search for products) and click in Show Report button

### If no show or not retuns data

### Se não exibir nenhum dado tente efetuar o reindex para coletar os dados

Execute Magento2 CLI Command :

```
### php -f bin/magento index:reindex
```

After command finish , go to Magento2 Admin Panel > Reports and try execute Report Bestsellers again.


## Acknowledgments

* Magento2 Development Systems
* PHP
* Linux


### For questions please contact us:
``` 
Open new Issue. Thanks !
```
