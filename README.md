# Plaid API Error Codes

This repository contains a JSONL file with detailed information about various error codes from the Plaid API. The data has been scraped from the [Plaid API documentation](https://plaid.com/docs/errors) to provide a machine-readable reference for analytics engineers working with Plaid API data or logs.

## File Contents

The file `plaid_error_codes.jsonl` includes the following fields for each error code:


- **url**: The URL to the Plaid documentation page for the error. 
- **error_code**: The specific error code returned by the Plaid API.
- **error_description**: A brief description of the error.
- **common_causes**: A detailed explanation of common causes for the error.
- **common_causes_html**: The HTML formatted version of the common causes.
- **troubleshooting_steps**: Suggested steps to troubleshoot and resolve the error.
- **troubleshooting_steps_html**: The HTML formatted version of the troubleshooting steps.
- **api_error_response_html**: An example of the API error response in HTML format.

## Example Record 

```json
{
  "url": "https://plaid.com/docs/errors/income/",
  "error_code": "INCOME_VERIFICATION_DOCUMENT_NOT_FOUND",
  "error_description": "The requested income verification document was not found.",
  "common_causes": "The document URL is incorrect (for example, it may contain a typo) or has expired. The document URL has already been accessed. Document URLs can only be used once.",
  "common_causes_html": "<ul class=\"MDXComponents_ul__IBs4A\"><li>The document URL is incorrect (for example, it may contain a typo) or has expired.</li><li>The document URL has already been accessed. Document URLs can only be used once.</li></ul>",
  "troubleshooting_steps": "Check that the document URL is entered correctly. Make a new call to /credit/payroll_income/get to generate a new document URL.",
  "troubleshooting_steps_html": "<p>Check that the document URL is entered correctly.</p><p>Make a new call to <a href=\"/docs/api/products/income/#creditpayroll_incomeget\"><code>/credit/payroll_income/get</code></a> to generate a new document URL.</p>",
  "api_error_response_html": "<code class=\"CodeBlock-module_code__18Tbe\"><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">1</span><span class=\"token plain\">http code </span><span class=\"token number\" style=\"color:#fce76b\">400</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">2</span><span class=\"token plain\"></span><span class=\"token punctuation\" style=\"color:#adadad\">{</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">3</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"error_type\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token string\" style=\"color:#abffdb\">\"INCOME_VERIFICATION_ERROR\"</span><span class=\"token punctuation\" style=\"color:#adadad\">,</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">4</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"error_code\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token string\" style=\"color:#abffdb\">\"INCOME_VERIFICATION_DOCUMENT_NOT_FOUND\"</span><span class=\"token punctuation\" style=\"color:#adadad\">,</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">5</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"error_message\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token string\" style=\"color:#abffdb\">\"the requested data was not found. Please check the ID supplied.\"</span><span class=\"token punctuation\" style=\"color:#adadad\">,</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">6</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"display_message\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token null keyword\" style=\"color:#63daff\">null</span><span class=\"token punctuation\" style=\"color:#adadad\">,</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">7</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"request_id\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token string\" style=\"color:#abffdb\">\"HNTDNrA8F1shFEW\"</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">8</span><span class=\"token plain\"></span><span class=\"token punctuation\" style=\"color:#adadad\">}</span></div></code>"
}
```

## Usage 

The JSONL file can be loaded into a database or used in a internal company application to provide detailed information about error codes. The purpose for including the HTML blocks is to make this information easier to embed, if needed. You should always refer to the [Plaid API documentation](https://plaid.com/docs/errors/) for the most accurate and up to date information. I do not guarantee that this file is up to date with the latest error codes.

