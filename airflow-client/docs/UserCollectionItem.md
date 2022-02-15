

# UserCollectionItem

A user object.  *New in version 2.1.0* 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**firstName** | **String** | The user&#39;s first name.  *Changed in version 2.2.0*&amp;#58; A minimum character length requirement (&#39;minLength&#39;) is added.  |  [optional]
**lastName** | **String** | The user&#39;s last name.  *Changed in version 2.2.0*&amp;#58; A minimum character length requirement (&#39;minLength&#39;) is added.  |  [optional]
**username** | **String** | The username.  *Changed in version 2.2.0*&amp;#58; A minimum character length requirement (&#39;minLength&#39;) is added.  |  [optional]
**email** | **String** | The user&#39;s email.  *Changed in version 2.2.0*&amp;#58; A minimum character length requirement (&#39;minLength&#39;) is added.  |  [optional]
**active** | **Boolean** | Whether the user is active |  [optional] [readonly]
**lastLogin** | **String** | The last user login |  [optional] [readonly]
**loginCount** | **Integer** | The login count |  [optional] [readonly]
**failedLoginCount** | **Integer** | The number of times the login failed |  [optional] [readonly]
**roles** | [**List&lt;UserCollectionItemRoles&gt;**](UserCollectionItemRoles.md) | User roles.  *Changed in version 2.2.0*&amp;#58; Field is no longer read-only.  |  [optional]
**createdOn** | **String** | The date user was created |  [optional] [readonly]
**changedOn** | **String** | The date user was changed |  [optional] [readonly]



