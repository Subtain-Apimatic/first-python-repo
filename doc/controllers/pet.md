# Pet

Everything about your Pets

Find out more: [http://swagger.io](http://swagger.io)

```python
pet_controller = client.pet
```

## Class Name

`PetController`

## Methods

* [Upload File](../../doc/controllers/pet.md#upload-file)
* [Inpet](../../doc/controllers/pet.md#inpet)
* [Update an Pet](../../doc/controllers/pet.md#update-an-pet)
* [Find Pet in the Status](../../doc/controllers/pet.md#find-pet-in-the-status)
* [Find Pets an Tags](../../doc/controllers/pet.md#find-pets-an-tags)
* [Get Pet by Id](../../doc/controllers/pet.md#get-pet-by-id)
* [Update Pet With Form](../../doc/controllers/pet.md#update-pet-with-form)
* [Delete Pet](../../doc/controllers/pet.md#delete-pet)


# Upload File

uploads an image

```python
def upload_file(self,
               pet_id,
               additional_metadata=None,
               file=None)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pet_id` | `long\|int` | Template, Required | ID of pet to update |
| `additional_metadata` | `string` | Form, Optional | Additional data to pass to server |
| `file` | `typing.BinaryIO` | Form, Optional | file to upload |

## Response Type

[`ApiResponse`](../../doc/models/api-response.md)

## Example Usage

```python
pet_id = 152

result = pet_controller.upload_file(pet_id)
print(result)
```


# Inpet

Add a new pet to the store

```python
def inpet(self,
         body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Pet`](../../doc/models/pet.md) | Body, Required | Pet object that needs to be added to the store |

## Response Type

`void`

## Example Usage

```python
body = Pet(
    name='name6',
    photo_urls=[
        'photoUrls1'
    ]
)

result = pet_controller.inpet(body)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 405 | Invalid input | `APIException` |


# Update an Pet

Update an existing pet

```python
def update_an_pet(self,
                 body)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `body` | [`Pet`](../../doc/models/pet.md) | Body, Required | Pet object that needs to be added to the store |

## Response Type

`void`

## Example Usage

```python
body = Pet(
    name='name6',
    photo_urls=[
        'photoUrls1'
    ]
)

result = pet_controller.update_an_pet(body)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid ID supplied | `APIException` |
| 404 | Pet not found | `APIException` |
| 405 | Validation exception | `APIException` |


# Find Pet in the Status

Multiple status values can be provided with comma separated strings

```python
def find_pet_in_the_status(self,
                          status)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`List of Status2Enum`](../../doc/models/status-2-enum.md) | Query, Required | Status values that need to be considered for filter |

## Response Type

[`List of Pet`](../../doc/models/pet.md)

## Example Usage

```python
status = [
    Status2Enum.PENDING,
    Status2Enum.SOLD,
    Status2Enum.AVAILABLE
]

result = pet_controller.find_pet_in_the_status(status)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid status value | `APIException` |


# Find Pets an Tags

**This endpoint is deprecated.**

Multiple tags can be provided with comma separated strings. Use tag1, tag2, tag3 for testing.

```python
def find_pets_an_tags(self,
                     tags)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `tags` | `List of string` | Query, Required | Tags to filter by |

## Response Type

[`List of Pet`](../../doc/models/pet.md)

## Example Usage

```python
tags = [
    'tags5',
    'tags6'
]

result = pet_controller.find_pets_an_tags(tags)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid tag value | `APIException` |


# Get Pet by Id

Returns a single pet

```python
def get_pet_by_id(self,
                 pet_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pet_id` | `long\|int` | Template, Required | ID of pet to return |

## Response Type

[`Pet`](../../doc/models/pet.md)

## Example Usage

```python
pet_id = 152

result = pet_controller.get_pet_by_id(pet_id)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid ID supplied | `APIException` |
| 404 | Pet not found | `APIException` |


# Update Pet With Form

Updates a pet in the store with form data

```python
def update_pet_with_form(self,
                        pet_id,
                        name=None,
                        status=None)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pet_id` | `long\|int` | Template, Required | ID of pet that needs to be updated |
| `name` | `string` | Form, Optional | Updated name of the pet |
| `status` | `string` | Form, Optional | Updated status of the pet |

## Response Type

`void`

## Example Usage

```python
pet_id = 152

result = pet_controller.update_pet_with_form(pet_id)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 405 | Invalid input | `APIException` |


# Delete Pet

Deletes a pet

```python
def delete_pet(self,
              pet_id,
              api_key=None)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pet_id` | `long\|int` | Template, Required | Pet id to delete |
| `api_key` | `string` | Header, Optional | - |

## Response Type

`void`

## Example Usage

```python
pet_id = 152

result = pet_controller.delete_pet(pet_id)
print(result)
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 400 | Invalid ID supplied | `APIException` |
| 404 | Pet not found | `APIException` |

