This guide provides information on:



## xbrlware REST API Resources ##

These resource paths are beneath http://www.xbrlware.com

In the paths below, <font color='#357EC7'><i><b>ci-key</b></i></font> represents the central index of the desired entity and <font color='#357EC7'><b><i>accession-key</i></b></font> represents a XBRL filing accession key. ci-key and accession-key **MAY** have leading zeroes.

If ci-key and accession-key sounds alien, have a look at GetStarted page.

Access to all resource paths require xbrlware API key. See GetStarted page for how to obtain an API key. Each request should contain a valid xbrlware API Key in http request header under name **Xbrlware-ApiKey**

### Entity related ###
|Method|Resource                                      |Description                                                           |
|:-----|:---------------------------------------------|:---------------------------------------------------------------------|
|GET   |/api/entities/<font color='#357EC7'><i><b>ci-key</b></i></font>|Fetch details about an entity. _**Note**_: This resource request doesn't require xbrlware API Key|
|GET   |/api/entities/<font color='#357EC7'><i><b>ci-key</b></i></font>/filings|Fetch details about all XBRL filings of an entity                     |


---


### Filing related ###
|Method|Resource                                      |Description                                                           |
|:-----|:---------------------------------------------|:---------------------------------------------------------------------|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>|Fetch details about a XBRL filing                                     |


---


### Reports related ###
|Method|Resource                                      |Description                                                           |
|:-----|:---------------------------------------------|:---------------------------------------------------------------------|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports|Fetch details about all xbrlware generated **html** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/pre|Fetch details about all xbrlware generated presentation **html** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/pre/json|Fetch details about all xbrlware generated presentation **json** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/pre/xml|Fetch details about all xbrlware generated presentation **xml** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/pre/xls|Fetch details about all xbrlware generated presentation **xls** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/cal|Fetch details about all xbrlware generated calculation **html** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/cal/json|Fetch details about all xbrlware generated calculation **json** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/cal/xml|Fetch details about all xbrlware generated calculation **xml** reports of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/reports/cal/xls|Fetch details about all xbrlware generated calculation **xls** reports of a XBRL filing|


---


### Data related ###
|Method|Resource                                      |Description                                                           |
|:-----|:---------------------------------------------|:---------------------------------------------------------------------|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/data/<font color='#357EC7'><b><i>fact_name</i></b></font>|Fetch details about a fact (ie US-GAPP element, like NetIncomeLoss, ProfitLoss, etc) of a XBRL filing|
|GET   |/api/filings/<font color='#357EC7'><b><i>accession-key</i></b></font>/data/<font color='#357EC7'>_<b>fact_name_1</b></font>,_<font color='#357EC7'>_<b>fact_name_2</b></font>,_<font color='#357EC7'><b><i>...</i></b></font>|Fetch details about multiple facts (ie US-GAPP element, like NetIncomeLoss, ProfitLoss, etc) of a XBRL filing, seperated by comma|


---
