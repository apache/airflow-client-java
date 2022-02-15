# ImportErrorApi

All URIs are relative to *http://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getImportError**](ImportErrorApi.md#getImportError) | **GET** /importErrors/{import_error_id} | Get an import error
[**getImportErrors**](ImportErrorApi.md#getImportErrors) | **GET** /importErrors | List import errors


<a name="getImportError"></a>
# **getImportError**
> ImportError getImportError(importErrorId)

Get an import error

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.ImportErrorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    ImportErrorApi apiInstance = new ImportErrorApi(defaultClient);
    Integer importErrorId = 56; // Integer | The import error ID.
    try {
      ImportError result = apiInstance.getImportError(importErrorId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportErrorApi#getImportError");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **importErrorId** | **Integer**| The import error ID. |

### Return type

[**ImportError**](ImportError.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |
**404** | A specified resource is not found. |  -  |

<a name="getImportErrors"></a>
# **getImportErrors**
> ImportErrorCollection getImportErrors(limit, offset, orderBy)

List import errors

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.ImportErrorApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    ImportErrorApi apiInstance = new ImportErrorApi(defaultClient);
    Integer limit = 100; // Integer | The numbers of items to return.
    Integer offset = 56; // Integer | The number of items to skip before starting to collect the result set.
    String orderBy = "orderBy_example"; // String | The name of the field to order the results by. Prefix a field name with `-` to reverse the sort order.  *New in version 2.1.0* 
    try {
      ImportErrorCollection result = apiInstance.getImportErrors(limit, offset, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ImportErrorApi#getImportErrors");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **limit** | **Integer**| The numbers of items to return. | [optional] [default to 100]
 **offset** | **Integer**| The number of items to skip before starting to collect the result set. | [optional]
 **orderBy** | **String**| The name of the field to order the results by. Prefix a field name with &#x60;-&#x60; to reverse the sort order.  *New in version 2.1.0*  | [optional]

### Return type

[**ImportErrorCollection**](ImportErrorCollection.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |

