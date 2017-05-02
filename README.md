# magento2-reports

Alternative solution for the problem with the Date format of Reports on Magento2.

## Getting Started

Downloading this project in Zip format and uncompress.

Copy folder Reports in your Magento2 Project , example:

<root_folder>/app/code/MyVendor/ .... paste Reports/ here.


### Prerequisites

#### Magento >= 2.1.5 


### Installing

After copied files and folders in app/code/<myvendor>/ run Magento2 CLI Command :  

```
### php -f bin/magento setup:upgrade

After

### php -f bin/magento cache:flush 

And 

### php -f bin/magento cache:clean 
```


## Running the tests

Open Magento2 Admin Panel , Go to Reports and Select Submenu Products and click in Bestsellers 

Type date initial and date finish (range to search for products) and click in Show Report button

### If no show or not retuns data

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
