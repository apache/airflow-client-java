# ProviderApi

All URIs are relative to *http://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getProviders**](ProviderApi.md#getProviders) | **GET** /providers | List providers


<a name="getProviders"></a>
# **getProviders**
> ProviderCollection getProviders()

List providers

Get a list of providers.  *New in version 2.1.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.ProviderApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    ProviderApi apiInstance = new ProviderApi(defaultClient);
    try {
      ProviderCollection result = apiInstance.getProviders();
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling ProviderApi#getProviders");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**ProviderCollection**](ProviderCollection.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of providers. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |

