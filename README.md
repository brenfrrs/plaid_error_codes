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
- **api_error_response_error_type**: The type of error as specified in the API response.
- **api_error_response_error_code**: The error code as specified in the API response.
- **api_error_response_error_message**: The error message as returned in the API response.
- **api_error_response_display_message**: The display message intended for end-users, as specified in the API response.

## Example Record 

```json
{
  "url": "https://plaid.com/docs/errors/item/",
  "error_code": "INVALID_CREDENTIALS",
  "error_description": "The financial institution indicated that the credentials provided were invalid.",
  "common_causes": "The user entered incorrect credentials at their selected institution.Extra spaces, capitalization, and punctuation errors are common causes of INVALID_CREDENTIALS.The institution requires special configuration steps before the user can link their account with Plaid. KeyBank, Interactive Brokers, and Betterment are examples of institutions that require this setup.The user selected the wrong institution.Plaid supports institutions that have multiple login portals for the various products they offer, and it is common for users to confuse a different selection for the one which their credentials would actually be accepted.This confusion is particularly common between Vanguard (brokerage accounts) and My Vanguard Plan (retirement accounts). This is also common for users attempting to link prepaid stored-value cards, as many institutions have separate login portals specifically for those cards.",
  "common_causes_html": "<ul class=\"MDXComponents_ul__IBs4A\"><li>The user entered incorrect credentials at their selected institution.<ul class=\"MDXComponents_ul__IBs4A\"><li>Extra spaces, capitalization, and punctuation errors are common causes of <code>INVALID_CREDENTIALS</code>.</li></ul></li><li>The institution requires special configuration steps before the user can link their account with Plaid. KeyBank, Interactive Brokers, and Betterment are examples of institutions that require this setup.</li><li>The user selected the wrong institution.<ul class=\"MDXComponents_ul__IBs4A\"><li>Plaid supports institutions that have multiple login portals for the various products they offer, and it is common for users to confuse a different selection for the one which their credentials would actually be accepted.</li><li>This confusion is particularly common between Vanguard (brokerage accounts) and My Vanguard Plan (retirement accounts). This is also common for users attempting to link prepaid stored-value cards, as many institutions have separate login portals specifically for those cards.</li></ul></li></ul>",
  "troubleshooting_steps": "Prompt your user to retry entering their credentials.",
  "troubleshooting_steps_html": "<p>Prompt your user to retry entering their credentials.</p><p>Confirm that the credentials being entered are correct by asking the user to test logging in to their financial institution website using the same set of credentials.</p><p>The user should check their financial institution website for special settings to allow access for third-party apps, such as a \"third party application password\" or \"allow third party access\" setting.</p><p>Verify that the user is selecting the correct institution in Link’s Institution Select view.</p>",
  "api_error_response_html": "<code class=\"CodeBlock-module_code__18Tbe\"><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">1</span><span class=\"token plain\">http code </span><span class=\"token number\" style=\"color:#fce76b\">400</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">2</span><span class=\"token plain\"></span><span class=\"token punctuation\" style=\"color:#adadad\">{</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\" style=\"color:#ededed\"><span class=\"CodeBlock-module_lineNumbers__L4M3W\">3</span><span class=\"token plain\"> </span><span class=\"token property\" style=\"color:#ffaab9\">\"error_type\"</span><span class=\"token operator\" style=\"color:#adadad\">:</span><span class=\"token plain\"> </span><span class=\"token string\" style=\"color:#abffdb\">\"ITEM_ERROR\"</span><span class=\"token punctuation\" style=\"color:#adadad\">,</span><span class=\"token plain\"></span></div><div class=\"CodeBlock-module_line__IyeRg\"...(line too long; chars omitted)",
  "api_error_response_error_type": "ITEM_ERROR",
  "api_error_response_error_code": "INVALID_CREDENTIALS",
  "api_error_response_error_message": "the provided credentials were not correct",
  "api_error_response_display_message": "The provided credentials were not correct. Please try again."
}
```

## Usage 

The JSONL file can be loaded into a database or used in a internal company application to provide detailed information about error codes. The purpose for including the HTML blocks is to make this information easier to embed, if needed. You should always refer to the [Plaid API documentation](https://plaid.com/docs/errors/) for the most accurate and up to date information. I do not guarantee that this file is up to date with the latest error codes.

