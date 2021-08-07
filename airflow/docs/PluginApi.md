# PluginApi

All URIs are relative to *http://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**getPlugins**](PluginApi.md#getPlugins) | **GET** /plugins | Get a list of loaded plugins


<a name="getPlugins"></a>
# **getPlugins**
> PluginCollection getPlugins(limit, offset)

Get a list of loaded plugins

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.PluginApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    PluginApi apiInstance = new PluginApi(defaultClient);
    Integer limit = 100; // Integer | The numbers of items to return.
    Integer offset = 56; // Integer | The number of items to skip before starting to collect the result set.
    try {
      PluginCollection result = apiInstance.getPlugins(limit, offset);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling PluginApi#getPlugins");
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

### Return type

[**PluginCollection**](PluginCollection.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |
**404** | A specified resource is not found. |  -  |

