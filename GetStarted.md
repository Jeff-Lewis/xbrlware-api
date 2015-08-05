xbrlware API Key is required to get started with xbrlware REST API. API key can be obtained from [xbrlware.com/apikey](http://www.xbrlware.com/apikey)

Most API calls require central index key (ci-key) of a company. [SEC CIK Lookup](http://www.sec.gov/edgar/searchedgar/cik.htm) page might be helpful to obtain central index key of a company.

## Fetch details of xbrl filings of a company ##

In the following section, we will assume that company ci-key is 764180 and that your API key is my123key.

Lets fetch all XBRL filings by a company with ci-key 764180

```
curl -H "Xbrlware-ApiKey: my123key" http://www.xbrlware.com/api/entities/764180/filings
```

This will return JSON object such as

```
{
    "status":"ok",
    "error-code":"0",
    "error-desc":"",
    "results":[
        {
            "xbrl_pub_at":"Wed, 24 Feb 2010 16:13:00 +0530",
            "form_type":"10-K",
            "report_period":"2009-12-31",
            "ci_key":"764180",
            "fiscal_period":"1970-12-31",
            "edgar_url":"http://www.sec.gov/Archives/edgar/data/764180/000119312510039027/0001193125-10-039027-index.htm",
            "accession_key":"000119312510039027"
        }
    ]
}
```



"results" contains array of filings. In this case,  there is one xbrl filing for a company with ci-key 764180. **Note:** _Each filing is uniquely identified by accession-key_.

## Fetch xbrlware generated reports of a xbrl filing ##

To fetch xbrlware generated reports, we need ci-key and accession-key (see above example on how to get accession key of a XBRL filing)

Lets fetch xbrlware generated reports for ci-key 764180 and accession-key 000119312510039027

```
curl -H "Xbrlware-ApiKey: my123key" http://www.xbrlware.com/api/entities/764180/filings/000119312510039027/reports
```

This will return JSON object such as

```
{
    "status":"ok",
    "error-code":"0",
    "error-desc":"",
    "results":{
        "ci_key":"764180",
        "accession_key":"000119312510039027",
        "reports":{
            "pre":[
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Statement_Of_Shareholders_Equity_And_Other_Comprehensive_Income.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Total_Finance_Assets_Net_Of_Allowance_For_Losses_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Document_Information.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Statement_Of_Cash_Flows_Indirect.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Fair_Value_Measurement_Inputs_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Quarterly_Financial_Information_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Significant_Accounting_Policies_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Schedule_Of_Valuation_And_Qualifying_Accounts_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Derivative_Instruments_And_Hedging_Activities_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Long_Term_Debt_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Statement_Of_Financial_Position_Classified_Parenthetical.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Pension_And_Other_Postretirement_Benefits_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Comprehensive_Income_Note_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Schedule_Of_Stock_By_Class_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Statement_Of_Financial_Position_Classified.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Inventory_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Statement_Of_Income.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Disposal_Groups_Including_Discontinued_Operations_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Equity_Method_Investments_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Income_Tax_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Business_Combination_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Segment_Reporting_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Restructuring_And_Impairment_Charges_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Schedule_Of_Loss_Contingencies_By_Contingency_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Organization_Consolidation_And_Presentation_Of_Financial_Statements_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Earnings_Per_Share_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Goodwill_And_Intangible_Assets_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Entity_Information.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Disclosure_Of_Share_Based_Compensation_Arrangements_By_Share_Based_Payment_Award_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Additional_Financial_Information_Disclosure_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Schedule_Of_Condensed_Financial_Statements_Text_Block.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/pre/Notes_To_Financial_Statements_Short_Term_Debt_Text_Block.html"
            ],
            "cal":[
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/cal/Statement_Of_Shareholders_Equity_And_Other_Comprehensive_Income.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/cal/Statement_Of_Cash_Flows_Indirect.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/cal/Statement_Of_Financial_Position_Classified.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/cal/Statement_Of_Income.html",
                "http://xbrlware.s3.amazonaws.com/data/764180/000119312510039027/report/d64597b44dfa/cal/Statement_Of_Income_Alternate1.html"
            ]
        }
    }
}
```

[REST Resources](RESTResources.md) page contains list of REST Resources for [xbrlware.com](http://www.xbrlware.com)