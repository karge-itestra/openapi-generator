# FakeApi

All URIs are relative to *http://petstore.swagger.io:80/v2*

Method | HTTP request | Description
------------- | ------------- | -------------
[**fakeHealthGet**](FakeApi.md#fakeHealthGet) | **GET** /fake/health | Health check endpoint
[**fakeHttpSignatureTest**](FakeApi.md#fakeHttpSignatureTest) | **GET** /fake/http-signature-test | test http signature authentication
[**fakeOuterBooleanSerialize**](FakeApi.md#fakeOuterBooleanSerialize) | **POST** /fake/outer/boolean | 
[**fakeOuterCompositeSerialize**](FakeApi.md#fakeOuterCompositeSerialize) | **POST** /fake/outer/composite | 
[**fakeOuterNumberSerialize**](FakeApi.md#fakeOuterNumberSerialize) | **POST** /fake/outer/number | 
[**fakeOuterStringSerialize**](FakeApi.md#fakeOuterStringSerialize) | **POST** /fake/outer/string | 
[**fakePropertyEnumIntegerSerialize**](FakeApi.md#fakePropertyEnumIntegerSerialize) | **POST** /fake/property/enum-int | 
[**testBodyWithBinary**](FakeApi.md#testBodyWithBinary) | **PUT** /fake/body-with-binary | 
[**testBodyWithFileSchema**](FakeApi.md#testBodyWithFileSchema) | **PUT** /fake/body-with-file-schema | 
[**testBodyWithQueryParams**](FakeApi.md#testBodyWithQueryParams) | **PUT** /fake/body-with-query-params | 
[**testClientModel**](FakeApi.md#testClientModel) | **PATCH** /fake | To test \&quot;client\&quot; model
[**testEndpointParameters**](FakeApi.md#testEndpointParameters) | **POST** /fake | Fake endpoint for testing various parameters 假端點 偽のエンドポイント 가짜 엔드 포인트 
[**testEnumParameters**](FakeApi.md#testEnumParameters) | **GET** /fake | To test enum parameters
[**testGroupParameters**](FakeApi.md#testGroupParameters) | **DELETE** /fake | Fake endpoint to test group parameters (optional)
[**testInlineAdditionalProperties**](FakeApi.md#testInlineAdditionalProperties) | **POST** /fake/inline-additionalProperties | test inline additionalProperties
[**testJsonFormData**](FakeApi.md#testJsonFormData) | **GET** /fake/jsonFormData | test json serialization of form data
[**testQueryParameterCollectionFormat**](FakeApi.md#testQueryParameterCollectionFormat) | **PUT** /fake/test-query-paramters | 


<a name="fakeHealthGet"></a>
# **fakeHealthGet**
> HealthCheckResult fakeHealthGet()

Health check endpoint

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeHealthGet().execute(r -> r.prettyPeek());
```

### Parameters
This endpoint does not need any parameter.

### Return type

[**HealthCheckResult**](HealthCheckResult.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

<a name="fakeHttpSignatureTest"></a>
# **fakeHttpSignatureTest**
> fakeHttpSignatureTest(pet, query1, header1)

test http signature authentication

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeHttpSignatureTest()
    .body(pet).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pet** | [**Pet**](Pet.md)| Pet object that needs to be added to the store |
 **query1** | **String**| query parameter | [optional]
 **header1** | **String**| header parameter | [optional]

### Return type

null (empty response body)

### Authorization

[http_signature_test](../README.md#http_signature_test)

### HTTP request headers

 - **Content-Type**: application/json, application/xml
 - **Accept**: Not defined

<a name="fakeOuterBooleanSerialize"></a>
# **fakeOuterBooleanSerialize**
> Boolean fakeOuterBooleanSerialize(body)



Test serialization of outer boolean types

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeOuterBooleanSerialize().execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **Boolean**| Input boolean as post body | [optional]

### Return type

**Boolean**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="fakeOuterCompositeSerialize"></a>
# **fakeOuterCompositeSerialize**
> OuterComposite fakeOuterCompositeSerialize(outerComposite)



Test serialization of object with outer number type

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeOuterCompositeSerialize().execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **outerComposite** | [**OuterComposite**](OuterComposite.md)| Input composite as post body | [optional]

### Return type

[**OuterComposite**](OuterComposite.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="fakeOuterNumberSerialize"></a>
# **fakeOuterNumberSerialize**
> BigDecimal fakeOuterNumberSerialize(body)



Test serialization of outer number types

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeOuterNumberSerialize().execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **BigDecimal**| Input number as post body | [optional]

### Return type

[**BigDecimal**](BigDecimal.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="fakeOuterStringSerialize"></a>
# **fakeOuterStringSerialize**
> String fakeOuterStringSerialize(body)



Test serialization of outer string types

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakeOuterStringSerialize().execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **String**| Input string as post body | [optional]

### Return type

**String**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="fakePropertyEnumIntegerSerialize"></a>
# **fakePropertyEnumIntegerSerialize**
> OuterObjectWithEnumProperty fakePropertyEnumIntegerSerialize(outerObjectWithEnumProperty)



Test serialization of enum (int) properties with examples

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.fakePropertyEnumIntegerSerialize()
    .body(outerObjectWithEnumProperty).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **outerObjectWithEnumProperty** | [**OuterObjectWithEnumProperty**](OuterObjectWithEnumProperty.md)| Input enum (int) as post body |

### Return type

[**OuterObjectWithEnumProperty**](OuterObjectWithEnumProperty.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: */*

<a name="testBodyWithBinary"></a>
# **testBodyWithBinary**
> testBodyWithBinary(body)



For this test, the body has to be a binary file.

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testBodyWithBinary()
    .body(body).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | **File**| image to upload |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: image/png
 - **Accept**: Not defined

<a name="testBodyWithFileSchema"></a>
# **testBodyWithFileSchema**
> testBodyWithFileSchema(fileSchemaTestClass)



For this test, the body for this request must reference a schema named &#x60;File&#x60;.

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testBodyWithFileSchema()
    .body(fileSchemaTestClass).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **fileSchemaTestClass** | [**FileSchemaTestClass**](FileSchemaTestClass.md)|  |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="testBodyWithQueryParams"></a>
# **testBodyWithQueryParams**
> testBodyWithQueryParams(query, user)



### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testBodyWithQueryParams()
    .queryQuery(query)
    .body(user).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **String**|  |
 **user** | [**User**](User.md)|  |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="testClientModel"></a>
# **testClientModel**
> Client testClientModel(client)

To test \&quot;client\&quot; model

To test \&quot;client\&quot; model

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testClientModel()
    .body(client).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client** | [**Client**](Client.md)| client model |

### Return type

[**Client**](Client.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

<a name="testEndpointParameters"></a>
# **testEndpointParameters**
> testEndpointParameters(number, _double, patternWithoutDelimiter, _byte, integer, int32, int64, _float, string, binary, date, dateTime, password, paramCallback)

Fake endpoint for testing various parameters 假端點 偽のエンドポイント 가짜 엔드 포인트 

Fake endpoint for testing various parameters 假端點 偽のエンドポイント 가짜 엔드 포인트 

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testEndpointParameters()
    .numberForm(number)
    ._doubleForm(_double)
    .patternWithoutDelimiterForm(patternWithoutDelimiter)
    ._byteForm(_byte).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **number** | **BigDecimal**| None |
 **_double** | **Double**| None |
 **patternWithoutDelimiter** | **String**| None |
 **_byte** | **byte[]**| None |
 **integer** | **Integer**| None | [optional]
 **int32** | **Integer**| None | [optional]
 **int64** | **Long**| None | [optional]
 **_float** | **Float**| None | [optional]
 **string** | **String**| None | [optional]
 **binary** | **File**| None | [optional]
 **date** | **LocalDate**| None | [optional]
 **dateTime** | **OffsetDateTime**| None | [optional]
 **password** | **String**| None | [optional]
 **paramCallback** | **String**| None | [optional]

### Return type

null (empty response body)

### Authorization

[http_basic_test](../README.md#http_basic_test)

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

<a name="testEnumParameters"></a>
# **testEnumParameters**
> testEnumParameters(enumHeaderStringArray, enumHeaderString, enumQueryStringArray, enumQueryString, enumQueryInteger, enumQueryDouble, enumFormStringArray, enumFormString)

To test enum parameters

To test enum parameters

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testEnumParameters().execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **enumHeaderStringArray** | [**List&lt;String&gt;**](String.md)| Header parameter enum test (string array) | [optional] [enum: >, $]
 **enumHeaderString** | **String**| Header parameter enum test (string) | [optional] [default to -efg] [enum: _abc, -efg, (xyz)]
 **enumQueryStringArray** | [**List&lt;String&gt;**](String.md)| Query parameter enum test (string array) | [optional] [enum: >, $]
 **enumQueryString** | **String**| Query parameter enum test (string) | [optional] [default to -efg] [enum: _abc, -efg, (xyz)]
 **enumQueryInteger** | **Integer**| Query parameter enum test (double) | [optional] [enum: 1, -2]
 **enumQueryDouble** | **Double**| Query parameter enum test (double) | [optional] [enum: 1.1, -1.2]
 **enumFormStringArray** | [**List&lt;String&gt;**](String.md)| Form parameter enum test (string array) | [optional] [default to $] [enum: >, $]
 **enumFormString** | **String**| Form parameter enum test (string) | [optional] [default to -efg] [enum: _abc, -efg, (xyz)]

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

<a name="testGroupParameters"></a>
# **testGroupParameters**
> testGroupParameters(requiredStringGroup, requiredBooleanGroup, requiredInt64Group, stringGroup, booleanGroup, int64Group)

Fake endpoint to test group parameters (optional)

Fake endpoint to test group parameters (optional)

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testGroupParameters()
    .requiredStringGroupQuery(requiredStringGroup)
    .requiredBooleanGroupHeader(requiredBooleanGroup)
    .requiredInt64GroupQuery(requiredInt64Group).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requiredStringGroup** | **Integer**| Required String in group parameters |
 **requiredBooleanGroup** | **Boolean**| Required Boolean in group parameters |
 **requiredInt64Group** | **Long**| Required Integer in group parameters |
 **stringGroup** | **Integer**| String in group parameters | [optional]
 **booleanGroup** | **Boolean**| Boolean in group parameters | [optional]
 **int64Group** | **Long**| Integer in group parameters | [optional]

### Return type

null (empty response body)

### Authorization

[bearer_test](../README.md#bearer_test)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

<a name="testInlineAdditionalProperties"></a>
# **testInlineAdditionalProperties**
> testInlineAdditionalProperties(requestBody)

test inline additionalProperties

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testInlineAdditionalProperties()
    .body(requestBody).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **requestBody** | [**Map&lt;String, String&gt;**](String.md)| request body |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

<a name="testJsonFormData"></a>
# **testJsonFormData**
> testJsonFormData(param, param2)

test json serialization of form data

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testJsonFormData()
    .paramForm(param)
    .param2Form(param2).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **param** | **String**| field1 |
 **param2** | **String**| field2 |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

<a name="testQueryParameterCollectionFormat"></a>
# **testQueryParameterCollectionFormat**
> testQueryParameterCollectionFormat(pipe, ioutil, http, url, context)



To test the collection format in query parameters

### Example
```java
// Import classes:
//import org.openapitools.client.ApiClient;
//import io.restassured.builder.RequestSpecBuilder;
//import io.restassured.filter.log.ErrorLoggingFilter;

FakeApi api = ApiClient.api(ApiClient.Config.apiConfig().withReqSpecSupplier(
                () -> new RequestSpecBuilder()
                        .setBaseUri("http://petstore.swagger.io:80/v2"))).fake();

api.testQueryParameterCollectionFormat()
    .pipeQuery(pipe)
    .ioutilQuery(ioutil)
    .httpQuery(http)
    .urlQuery(url)
    .contextQuery(context).execute(r -> r.prettyPeek());
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **pipe** | [**List&lt;String&gt;**](String.md)|  |
 **ioutil** | [**List&lt;String&gt;**](String.md)|  |
 **http** | [**List&lt;String&gt;**](String.md)|  |
 **url** | [**List&lt;String&gt;**](String.md)|  |
 **context** | [**List&lt;String&gt;**](String.md)|  |

### Return type

null (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined
