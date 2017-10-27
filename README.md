# magento2.2-traduccion-chile
# Magento 2 Spanish Language Pack Chile version 1.0.1

Spanish translation for Magento 2.2.0 Translation es_CL (Spanish Chile).

Traduction de Magento 2 en Spanish.

See documentation: https://www.magentochile.cl/m2-spanish-language-pack.html


## Supported versions

* Magento v2.2.0


## Links

* Website: https://www.magentochile.cl/
* Packagist: https://packagist.org/packages/magentochile/magento2-traduccion-chile
* Github: https://github.com/magentochile/magento2-traduccion-chile/
* Official version: https://www.magentochile.cl/m2-spanish-language-pack.html

## BUG Magento 2 #7502
For some strange reason, and most likely it is a Magento 2 bug, it is that it does not update the shopping cart. It has been tested with es_CL and does not start the update of the cart.

The solution the BUG #7502? At the moment, until Magento 2 fixes Bug #7502, you should add the following to your vendor/magento/zendframework1/library/Zend/Locale/Data/es_419.xml file the following, after decimalFormats numberSystem="latn":

      		<decimalFormats numberSystem="latn">
			<!-- Bug Magento 2 reported: https://github.com/magento/magento2/issues/7502 -->
			<!-- This part is new  -->
			<decimalFormatLength>
				<decimalFormat>
					<pattern>#,##0.###</pattern>
				</decimalFormat>
			</decimalFormatLength>
			<!--  End of the added part -->
			<!-- End Bug Magento 2 reported: https://github.com/magento/magento2/issues/7502 -->



## Official version
Remember that for a translation if you want a more complete translation and adapted to the country Chile, you can acquire the official language pack of Magento Chile in: https://www.magentochile.cl/m2-spanish-language-pack.html

## Important Note: 
This pack of languages, only contains the skeleton for translations (Not translated), which you can install and once installed can translate the file vendor/magentochile/magento2-traduccion-chile/es_CL.csv respectively.

## Installation
composer require magentochile/magento2.2-traduccion-chile dev-master

php bin/magento cache:clean

## End
