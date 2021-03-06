# IO.Swagger - the PowerShell module for the Swagger Petstore

This spec is mainly for testing Petstore server and contains fake endpoints, models. Please do not use this for any other purpose. Special characters: \" \\

This PowerShell module is automatically generated by the [Swagger Codegen](https://github.com/swagger-api/swagger-codegen) project:

- API version: 1.0.0
- SDK version: 1.0.0
- Build package: io.swagger.codegen.languages.CSharpClientCodegen

<a name="frameworks-supported"></a>
## Frameworks supported
- PowerShell 3.0 or later
- .NET 4.0 or later

<a name="dependencies"></a>
## Dependencies
- [RestSharp](https://www.nuget.org/packages/RestSharp) - 105.1.0 or later
- [Json.NET](https://www.nuget.org/packages/Newtonsoft.Json/) - 7.0.0 or later

The DLLs included in the package may not be the latest version. We recommend using [NuGet] (https://docs.nuget.org/consume/installing-nuget) to obtain the latest version of the packages:
```
Install-Package RestSharp
Install-Package Newtonsoft.Json
```

NOTE: RestSharp versions greater than 105.1.0 have a bug which causes file uploads to fail. See [RestSharp#742](https://github.com/restsharp/RestSharp/issues/742)

<a name="installation"></a>
## Installation
Run the following command to generate the DLL
- [Windows] `build.ps1`

Then import module from the `.\src\IO.Swagger` folder:
```posh
Import-Module -Name '.\src\IO.Swagger'
```
<a name="getting-started"></a>
## Getting Started

```posh
Set-ApiCredential -AccessToken 'YOUR_ACCESS_TOKEN'

New-Pet -Id 1 -Name 'foo' -Category (
    New-Category -Id 2 -Name 'bar'
) -PhotoUrls @(
    'http://example.com/foo',
    'http://example.com/bar'
) -Tags (
    New-Tag -Id 3 -Name 'baz'
) -Status Available | Update-Pet

Get-PetById -Id 1
```

<a name="documentation-for-api-endpoints"></a>
## Documentation for API Endpoints

All URIs are relative to *http://petstore.swagger.io:80/v2*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*FakeApi* | [**TestClientModel**](docs/FakeApi.md#testclientmodel) | **PATCH** /fake | To test \"client\" model
*FakeApi* | [**TestEndpointParameters**](docs/FakeApi.md#testendpointparameters) | **POST** /fake | Fake endpoint for testing various parameters 假端點 偽のエンドポイント 가짜 엔드 포인트 
*FakeApi* | [**TestEnumParameters**](docs/FakeApi.md#testenumparameters) | **GET** /fake | To test enum parameters
*PetApi* | [**AddPet**](docs/PetApi.md#addpet) | **POST** /pet | Add a new pet to the store
*PetApi* | [**DeletePet**](docs/PetApi.md#deletepet) | **DELETE** /pet/{petId} | Deletes a pet
*PetApi* | [**FindPetsByStatus**](docs/PetApi.md#findpetsbystatus) | **GET** /pet/findByStatus | Finds Pets by status
*PetApi* | [**FindPetsByTags**](docs/PetApi.md#findpetsbytags) | **GET** /pet/findByTags | Finds Pets by tags
*PetApi* | [**GetPetById**](docs/PetApi.md#getpetbyid) | **GET** /pet/{petId} | Find pet by ID
*PetApi* | [**UpdatePet**](docs/PetApi.md#updatepet) | **PUT** /pet | Update an existing pet
*PetApi* | [**UpdatePetWithForm**](docs/PetApi.md#updatepetwithform) | **POST** /pet/{petId} | Updates a pet in the store with form data
*PetApi* | [**UploadFile**](docs/PetApi.md#uploadfile) | **POST** /pet/{petId}/uploadImage | uploads an image
*StoreApi* | [**DeleteOrder**](docs/StoreApi.md#deleteorder) | **DELETE** /store/order/{order_id} | Delete purchase order by ID
*StoreApi* | [**GetInventory**](docs/StoreApi.md#getinventory) | **GET** /store/inventory | Returns pet inventories by status
*StoreApi* | [**GetOrderById**](docs/StoreApi.md#getorderbyid) | **GET** /store/order/{order_id} | Find purchase order by ID
*StoreApi* | [**PlaceOrder**](docs/StoreApi.md#placeorder) | **POST** /store/order | Place an order for a pet
*UserApi* | [**CreateUser**](docs/UserApi.md#createuser) | **POST** /user | Create user
*UserApi* | [**CreateUsersWithArrayInput**](docs/UserApi.md#createuserswitharrayinput) | **POST** /user/createWithArray | Creates list of users with given input array
*UserApi* | [**CreateUsersWithListInput**](docs/UserApi.md#createuserswithlistinput) | **POST** /user/createWithList | Creates list of users with given input array
*UserApi* | [**DeleteUser**](docs/UserApi.md#deleteuser) | **DELETE** /user/{username} | Delete user
*UserApi* | [**GetUserByName**](docs/UserApi.md#getuserbyname) | **GET** /user/{username} | Get user by user name
*UserApi* | [**LoginUser**](docs/UserApi.md#loginuser) | **GET** /user/login | Logs user into the system
*UserApi* | [**LogoutUser**](docs/UserApi.md#logoutuser) | **GET** /user/logout | Logs out current logged in user session
*UserApi* | [**UpdateUser**](docs/UserApi.md#updateuser) | **PUT** /user/{username} | Updated user


<a name="documentation-for-models"></a>
## Documentation for Models

 - [Model.AdditionalPropertiesClass](docs/AdditionalPropertiesClass.md)
 - [Model.Animal](docs/Animal.md)
 - [Model.AnimalFarm](docs/AnimalFarm.md)
 - [Model.ApiResponse](docs/ApiResponse.md)
 - [Model.ArrayOfArrayOfNumberOnly](docs/ArrayOfArrayOfNumberOnly.md)
 - [Model.ArrayOfNumberOnly](docs/ArrayOfNumberOnly.md)
 - [Model.ArrayTest](docs/ArrayTest.md)
 - [Model.Capitalization](docs/Capitalization.md)
 - [Model.Cat](docs/Cat.md)
 - [Model.Category](docs/Category.md)
 - [Model.ClassModel](docs/ClassModel.md)
 - [Model.Dog](docs/Dog.md)
 - [Model.EnumArrays](docs/EnumArrays.md)
 - [Model.EnumClass](docs/EnumClass.md)
 - [Model.EnumTest](docs/EnumTest.md)
 - [Model.FormatTest](docs/FormatTest.md)
 - [Model.HasOnlyReadOnly](docs/HasOnlyReadOnly.md)
 - [Model.List](docs/List.md)
 - [Model.MapTest](docs/MapTest.md)
 - [Model.MixedPropertiesAndAdditionalPropertiesClass](docs/MixedPropertiesAndAdditionalPropertiesClass.md)
 - [Model.Model200Response](docs/Model200Response.md)
 - [Model.ModelClient](docs/ModelClient.md)
 - [Model.ModelReturn](docs/ModelReturn.md)
 - [Model.Name](docs/Name.md)
 - [Model.NumberOnly](docs/NumberOnly.md)
 - [Model.Order](docs/Order.md)
 - [Model.OuterEnum](docs/OuterEnum.md)
 - [Model.Pet](docs/Pet.md)
 - [Model.ReadOnlyFirst](docs/ReadOnlyFirst.md)
 - [Model.SpecialModelName](docs/SpecialModelName.md)
 - [Model.Tag](docs/Tag.md)
 - [Model.User](docs/User.md)


<a name="documentation-for-authorization"></a>
## Documentation for Authorization

<a name="api_key"></a>
### api_key

- **Type**: API key
- **API key parameter name**: api_key
- **Location**: HTTP header

<a name="http_basic_test"></a>
### http_basic_test

- **Type**: HTTP basic authentication

<a name="petstore_auth"></a>
### petstore_auth

- **Type**: OAuth
- **Flow**: implicit
- **Authorization URL**: http://petstore.swagger.io/api/oauth/dialog
- **Scopes**: 
  - write:pets: modify pets in your account
  - read:pets: read your pets
