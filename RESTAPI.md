This guide provides information on:



## About ##

[xbrlware.com](http://www.xbrlware.com) exposes data and analyzed financial reports via simple RESTful interface that returns [JSON](http://www.json.org) encoded results that are easily processed by most languages and runtimes. In most cases, the method supported is **GET** and the response format is a [JSON](http://www.json.org) encoded result set with embedded status codes.

## API Request and Response ##
### Anatomy of Request ###
Each request should contain a valid [xbrlware API Key](http://www.xbrlware.com/apikey) in http request header under name **Xbrlware-ApiKey** . By providing a key, your application provides us with a identification mechanism.
### Anatomy of Reponse ###
Any REST request to xbrlware.com will receive JSON response. Every JSON response will have
  * status - "ok" or "fail"
  * error-code
    * "0" if status is "ok",
    * 3 digit error code as described in [List of error codes](ExceptionHandling#List_of_error_codes_and_description.md), if status is "fail"
  * error-desc
    * "" (empty string) if status is "ok"
    * Reason for failure as described in [List of error descriptions](ExceptionHandling#List_of_error_codes_and_description.md), if status is "fail"
  * results
    * Array containing results if status is "ok"
    * Empty array if status is "fail"

## Where to go from here? ##
  * [Get Started](GetStarted.md) - A quick introduction to xbrlware API
  * [REST Resources](RESTResources.md) - Descriptions of all xbrlware REST resources
  * [Exception Handling](ExceptionHandling.md) - List of error codes and details about JSON reponse when exception occurs
  * [Terms and Conditions](TermsAndConditions.md) - Terms of use