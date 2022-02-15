# UserApi

All URIs are relative to *http://localhost/api/v1*

Method | HTTP request | Description
------------- | ------------- | -------------
[**deleteUser**](UserApi.md#deleteUser) | **DELETE** /users/{username} | Delete a user
[**getUser**](UserApi.md#getUser) | **GET** /users/{username} | Get a user
[**getUsers**](UserApi.md#getUsers) | **GET** /users | List users
[**patchUser**](UserApi.md#patchUser) | **PATCH** /users/{username} | Update a user
[**postUser**](UserApi.md#postUser) | **POST** /users | Create a user


<a name="deleteUser"></a>
# **deleteUser**
> deleteUser(username)

Delete a user

Delete a user with a specific username.  *New in version 2.2.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.UserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    UserApi apiInstance = new UserApi(defaultClient);
    String username = "username_example"; // String | The username of the user.  *New in version 2.1.0* 
    try {
      apiInstance.deleteUser(username);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserApi#deleteUser");
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
 **username** | **String**| The username of the user.  *New in version 2.1.0*  |

### Return type

null (empty response body)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Success. |  -  |
**400** | Client specified an invalid argument. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |
**404** | A specified resource is not found. |  -  |

<a name="getUser"></a>
# **getUser**
> UserCollectionItem getUser(username)

Get a user

Get a user with a specific username.  *New in version 2.1.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.UserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    UserApi apiInstance = new UserApi(defaultClient);
    String username = "username_example"; // String | The username of the user.  *New in version 2.1.0* 
    try {
      UserCollectionItem result = apiInstance.getUser(username);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserApi#getUser");
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
 **username** | **String**| The username of the user.  *New in version 2.1.0*  |

### Return type

[**UserCollectionItem**](UserCollectionItem.md)

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

<a name="getUsers"></a>
# **getUsers**
> UserCollection getUsers(limit, offset, orderBy)

List users

Get a list of users.  *New in version 2.1.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.UserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    UserApi apiInstance = new UserApi(defaultClient);
    Integer limit = 100; // Integer | The numbers of items to return.
    Integer offset = 56; // Integer | The number of items to skip before starting to collect the result set.
    String orderBy = "orderBy_example"; // String | The name of the field to order the results by. Prefix a field name with `-` to reverse the sort order.  *New in version 2.1.0* 
    try {
      UserCollection result = apiInstance.getUsers(limit, offset, orderBy);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserApi#getUsers");
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

[**UserCollection**](UserCollection.md)

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

<a name="patchUser"></a>
# **patchUser**
> Role patchUser(username, user, updateMask)

Update a user

Update fields for a user.  *New in version 2.2.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.UserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    UserApi apiInstance = new UserApi(defaultClient);
    String username = "username_example"; // String | The username of the user.  *New in version 2.1.0* 
    User user = new User(); // User | 
    List<String> updateMask = Arrays.asList(); // List<String> | The fields to update on the resource. If absent or empty, all modifiable fields are updated. A comma-separated list of fully qualified names of fields. 
    try {
      Role result = apiInstance.patchUser(username, user, updateMask);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserApi#patchUser");
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
 **username** | **String**| The username of the user.  *New in version 2.1.0*  |
 **user** | [**User**](User.md)|  |
 **updateMask** | [**List&lt;String&gt;**](String.md)| The fields to update on the resource. If absent or empty, all modifiable fields are updated. A comma-separated list of fully qualified names of fields.  | [optional]

### Return type

[**Role**](Role.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success. |  -  |
**400** | Client specified an invalid argument. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |
**404** | A specified resource is not found. |  -  |

<a name="postUser"></a>
# **postUser**
> User postUser(user)

Create a user

Create a new user with unique username and email.  *New in version 2.2.0* 

### Example
```java
// Import classes:
import com.apache.airflow.client.ApiClient;
import com.apache.airflow.client.ApiException;
import com.apache.airflow.client.Configuration;
import com.apache.airflow.client.auth.*;
import com.apache.airflow.client.models.*;
import com.apache.airflow.client.api.UserApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost/api/v1");
    
    // Configure HTTP basic authorization: Basic
    HttpBasicAuth Basic = (HttpBasicAuth) defaultClient.getAuthentication("Basic");
    Basic.setUsername("YOUR USERNAME");
    Basic.setPassword("YOUR PASSWORD");


    UserApi apiInstance = new UserApi(defaultClient);
    User user = new User(); // User | 
    try {
      User result = apiInstance.postUser(user);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling UserApi#postUser");
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
 **user** | [**User**](User.md)|  |

### Return type

[**User**](User.md)

### Authorization

[Basic](../README.md#Basic), [Kerberos](../README.md#Kerberos)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success. |  -  |
**400** | Client specified an invalid argument. |  -  |
**401** | Request not authenticated due to missing, invalid, authentication info. |  -  |
**403** | Client does not have sufficient permission. |  -  |
**409** | An existing resource conflicts with the request. |  -  |

