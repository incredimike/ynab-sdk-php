# YNAB-SDK-PHP
Our API uses a REST based design, leverages the JSON data format, and relies upon HTTPS for transport. We respond with meaningful HTTP response codes and if an error occurs, we include error details in the response body.  API Documentation is at https://api.youneedabudget.com

This PHP package is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- Package version: 1.0.0
- Build package: io.swagger.codegen.languages.PhpClientCodegen

## Requirements

PHP 5.5 and later

## Installation & Usage
### Composer

To install the bindings via [Composer](http://getcomposer.org/), execute the following command:

```bash
$ composer require jorijn/ynab-sdk-php
```

### Manual Installation

Download the files and include `autoload.php`:

```php
    require_once('/path/to/YNAB-SDK-PHP/vendor/autoload.php');
```

## Tests

To run the unit tests:

```
composer install
./vendor/bin/phpunit
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: bearer
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKey('Authorization', 'YOUR_API_KEY');
$config = YNAB\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Authorization', 'Bearer');

$apiInstance = new YNAB\Api\AccountsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$budgetId = "budgetId_example"; // string | The ID of the Budget.
$accountId = "accountId_example"; // string | The ID of the Account.

try {
    $result = $apiInstance->getAccountById($budgetId, $accountId);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AccountsApi->getAccountById: ', $e->getMessage(), PHP_EOL;
}

?>
```

## Documentation for API Endpoints

All URIs are relative to *https://api.youneedabudget.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AccountsApi* | [**getAccountById**](docs/Api/AccountsApi.md#getaccountbyid) | **GET** /budgets/{budget_id}/accounts/{account_id} | Single account
*AccountsApi* | [**getAccounts**](docs/Api/AccountsApi.md#getaccounts) | **GET** /budgets/{budget_id}/accounts | Account list
*BudgetsApi* | [**getBudgetById**](docs/Api/BudgetsApi.md#getbudgetbyid) | **GET** /budgets/{budget_id} | Single budget
*BudgetsApi* | [**getBudgets**](docs/Api/BudgetsApi.md#getbudgets) | **GET** /budgets | List budgets
*CategoriesApi* | [**getCategories**](docs/Api/CategoriesApi.md#getcategories) | **GET** /budgets/{budget_id}/categories | List categories
*CategoriesApi* | [**getCategoryById**](docs/Api/CategoriesApi.md#getcategorybyid) | **GET** /budgets/{budget_id}/categories/{category_id} | Single category
*MonthsApi* | [**getBudgetMonth**](docs/Api/MonthsApi.md#getbudgetmonth) | **GET** /budgets/{budget_id}/months/{month} | Single budget month
*MonthsApi* | [**getBudgetMonths**](docs/Api/MonthsApi.md#getbudgetmonths) | **GET** /budgets/{budget_id}/months | List budget months
*PayeeLocationsApi* | [**getPayeeLocationById**](docs/Api/PayeeLocationsApi.md#getpayeelocationbyid) | **GET** /budgets/{budget_id}/payee_locations/{payee_location_id} | Single payee location
*PayeeLocationsApi* | [**getPayeeLocations**](docs/Api/PayeeLocationsApi.md#getpayeelocations) | **GET** /budgets/{budget_id}/payee_locations | List payee locations
*PayeeLocationsApi* | [**getPayeeLocationsByPayee**](docs/Api/PayeeLocationsApi.md#getpayeelocationsbypayee) | **GET** /budgets/{budget_id}/payees/{payee_id}/payee_locations | List locations for a payee
*PayeesApi* | [**getPayeeById**](docs/Api/PayeesApi.md#getpayeebyid) | **GET** /budgets/{budget_id}/payees/{payee_id} | Single payee
*PayeesApi* | [**getPayees**](docs/Api/PayeesApi.md#getpayees) | **GET** /budgets/{budget_id}/payees | List payees
*ScheduledTransactionsApi* | [**getScheduledTransactionById**](docs/Api/ScheduledTransactionsApi.md#getscheduledtransactionbyid) | **GET** /budgets/{budget_id}/scheduled_transactions/{scheduled_transaction_id} | Single scheduled transaction
*ScheduledTransactionsApi* | [**getScheduledTransactions**](docs/Api/ScheduledTransactionsApi.md#getscheduledtransactions) | **GET** /budgets/{budget_id}/scheduled_transactions | List scheduled transactions
*TransactionsApi* | [**bulkCreateTransactions**](docs/Api/TransactionsApi.md#bulkcreatetransactions) | **POST** /budgets/{budget_id}/transactions/bulk | Bulk create transactions
*TransactionsApi* | [**createTransaction**](docs/Api/TransactionsApi.md#createtransaction) | **POST** /budgets/{budget_id}/transactions | Create new transaction
*TransactionsApi* | [**getTransactions**](docs/Api/TransactionsApi.md#gettransactions) | **GET** /budgets/{budget_id}/transactions | List transactions
*TransactionsApi* | [**getTransactionsByAccount**](docs/Api/TransactionsApi.md#gettransactionsbyaccount) | **GET** /budgets/{budget_id}/accounts/{account_id}/transactions | List account transactions
*TransactionsApi* | [**getTransactionsByCategory**](docs/Api/TransactionsApi.md#gettransactionsbycategory) | **GET** /budgets/{budget_id}/categories/{category_id}/transactions | List category transactions
*TransactionsApi* | [**getTransactionsById**](docs/Api/TransactionsApi.md#gettransactionsbyid) | **GET** /budgets/{budget_id}/transactions/{transaction_id} | Single transaction
*TransactionsApi* | [**getTransactionsByPayee**](docs/Api/TransactionsApi.md#gettransactionsbypayee) | **GET** /budgets/{budget_id}/payees/{payee_id}/transactions | List payee transactions
*TransactionsApi* | [**updateTransaction**](docs/Api/TransactionsApi.md#updatetransaction) | **PUT** /budgets/{budget_id}/transactions/{transaction_id} | Updates an existing transaction
*UserApi* | [**getUser**](docs/Api/UserApi.md#getuser) | **GET** /user | User info


## Documentation For Models

 - [Account](docs/Model/Account.md)
 - [AccountResponse](docs/Model/AccountResponse.md)
 - [AccountWrapper](docs/Model/AccountWrapper.md)
 - [AccountsResponse](docs/Model/AccountsResponse.md)
 - [AccountsWrapper](docs/Model/AccountsWrapper.md)
 - [BudgetDetailResponse](docs/Model/BudgetDetailResponse.md)
 - [BudgetDetailWrapper](docs/Model/BudgetDetailWrapper.md)
 - [BudgetSummary](docs/Model/BudgetSummary.md)
 - [BudgetSummaryResponse](docs/Model/BudgetSummaryResponse.md)
 - [BudgetSummaryWrapper](docs/Model/BudgetSummaryWrapper.md)
 - [BulkIdWrapper](docs/Model/BulkIdWrapper.md)
 - [BulkIds](docs/Model/BulkIds.md)
 - [BulkResponse](docs/Model/BulkResponse.md)
 - [BulkTransactions](docs/Model/BulkTransactions.md)
 - [CategoriesResponse](docs/Model/CategoriesResponse.md)
 - [Category](docs/Model/Category.md)
 - [CategoryGroup](docs/Model/CategoryGroup.md)
 - [CategoryGroupsWrapper](docs/Model/CategoryGroupsWrapper.md)
 - [CategoryResponse](docs/Model/CategoryResponse.md)
 - [CategoryWrapper](docs/Model/CategoryWrapper.md)
 - [CurrencyFormat](docs/Model/CurrencyFormat.md)
 - [DateFormat](docs/Model/DateFormat.md)
 - [ErrorDetail](docs/Model/ErrorDetail.md)
 - [ErrorResponse](docs/Model/ErrorResponse.md)
 - [HybridTransactionsResponse](docs/Model/HybridTransactionsResponse.md)
 - [HybridTransactionsWrapper](docs/Model/HybridTransactionsWrapper.md)
 - [MonthDetailResponse](docs/Model/MonthDetailResponse.md)
 - [MonthDetailWrapper](docs/Model/MonthDetailWrapper.md)
 - [MonthSummariesResponse](docs/Model/MonthSummariesResponse.md)
 - [MonthSummariesWrapper](docs/Model/MonthSummariesWrapper.md)
 - [MonthSummary](docs/Model/MonthSummary.md)
 - [Payee](docs/Model/Payee.md)
 - [PayeeLocation](docs/Model/PayeeLocation.md)
 - [PayeeLocationResponse](docs/Model/PayeeLocationResponse.md)
 - [PayeeLocationWrapper](docs/Model/PayeeLocationWrapper.md)
 - [PayeeLocationsResponse](docs/Model/PayeeLocationsResponse.md)
 - [PayeeLocationsWrapper](docs/Model/PayeeLocationsWrapper.md)
 - [PayeeResponse](docs/Model/PayeeResponse.md)
 - [PayeeWrapper](docs/Model/PayeeWrapper.md)
 - [PayeesResponse](docs/Model/PayeesResponse.md)
 - [PayeesWrapper](docs/Model/PayeesWrapper.md)
 - [SaveTransaction](docs/Model/SaveTransaction.md)
 - [SaveTransactionWrapper](docs/Model/SaveTransactionWrapper.md)
 - [ScheduledSubTransaction](docs/Model/ScheduledSubTransaction.md)
 - [ScheduledTransactionResponse](docs/Model/ScheduledTransactionResponse.md)
 - [ScheduledTransactionSummary](docs/Model/ScheduledTransactionSummary.md)
 - [ScheduledTransactionWrapper](docs/Model/ScheduledTransactionWrapper.md)
 - [ScheduledTransactionsResponse](docs/Model/ScheduledTransactionsResponse.md)
 - [ScheduledTransactionsWrapper](docs/Model/ScheduledTransactionsWrapper.md)
 - [SubTransaction](docs/Model/SubTransaction.md)
 - [TransactionResponse](docs/Model/TransactionResponse.md)
 - [TransactionSummary](docs/Model/TransactionSummary.md)
 - [TransactionWrapper](docs/Model/TransactionWrapper.md)
 - [TransactionsResponse](docs/Model/TransactionsResponse.md)
 - [TransactionsWrapper](docs/Model/TransactionsWrapper.md)
 - [User](docs/Model/User.md)
 - [UserResponse](docs/Model/UserResponse.md)
 - [UserWrapper](docs/Model/UserWrapper.md)
 - [BudgetDetail](docs/Model/BudgetDetail.md)
 - [CategoryGroupWithCategories](docs/Model/CategoryGroupWithCategories.md)
 - [HybridTransaction](docs/Model/HybridTransaction.md)
 - [MonthDetail](docs/Model/MonthDetail.md)
 - [ScheduledTransactionDetail](docs/Model/ScheduledTransactionDetail.md)
 - [TransactionDetail](docs/Model/TransactionDetail.md)


## Documentation For Authorization


## bearer

- **Type**: API key
- **API key parameter name**: Authorization
- **Location**: HTTP header


## Author




