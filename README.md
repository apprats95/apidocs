# Authentication APIs


# LOGIN API
To Login Account and generate token for API validation

### Prerequisites
There is no Prerequistes for this API

### HTTP Request

```
/irrc/login
```

### Request headers

|    Name    |       Value     |
|:-----------|:----------------|
|Content-Type|application/json|

### Request body

| Parameter | Type |           Description     |
|:----------|:-----|:--------------------------|
|login|String|Username provided for login|
|password|String|Secret password for login|


### Example

##### Request

```
{
  "params": {
    "login": "user@mail.com",
    "password": "1234"
  }
}
```

##### Response

```
{
    "jsonrpc": "2.0",
    "id": null,
    "result": {
        "meta": {
            "status": true,
            "message": "Login Successfully!"
        },
        "data": {
            "user_id": 24,
            "token": "8f693a2c9225cccd4306d4343434334e648c715d66c040de38da9fb193d10a1c8cd42c2134fb598e43e0a8ca6e82bf65ed2a48ea0e184ca2595f71cbf892f",
            "name": "Store Manager",
            "contact_id": 137,
            "contact_name": "Store Manager",
            "email": "sample@mail.com",
            "mobile": "",
            "is_internal": true,
            "is_external": false,
            "is_system_admin": false,
            "is_director": false,
            "is_manager": false,
            "is_operations": false,
            "is_store_manager": true,
            "is_volunteer": false,
            "is_lead_volunteer": false
        }
    }
}
```

### Remarks

#  LOGOUT API

To Logout Account and clear token.

### Prerequisites
There is no Prerequistes for this API

### HTTP Request

```
/irrc/logout
```

### Request headers

|    Name    |       Value     |
|:-----------|:----------------|
|Content-Type|application/json|
|TOKEN|aqsw3sakskwj32kj3k2j33j2j3k23kj2k3j|

### Request body

| Parameter | Type |           Description     |
|:----------|:-----|:--------------------------|

Pass Empty Json : {}

### Example

##### Request

```
{ 
}
```

##### Response

```
{
    "jsonrpc": "2.0",
    "id": null,
    "result": {
        "meta": {
            "status": true,
            "message": "Logout Successfully!"
        },
        "data": {}
    }
}
```

### Remarks


#  CHANGE USER PASSWORD API

To change Logged-in User's Password

### Prerequisites
There is no Prerequistes for this API

### HTTP Request

```
/irrc/change_user_password
```

### Request headers

|    Name    |       Value     |
|:-----------|:----------------|
|Content-Type|application/json|
|TOKEN|aqsw3sakskwj32kj3k2j33j2j3k23kj2k3j|

### Request body

| Parameter | Type |           Description     |
|:----------|:-----|:--------------------------|
|old_password|String|Existing password|
|new_password|String|New password|


### Example

##### Request

```
{
  "params": {
    "old_password": "admin@1234",
    "new_password": "1234Admin"
  }
}
```

##### Response

```
{
    "jsonrpc": "2.0",
    "id": null,
    "result": {
        "meta": {
            "status": true,
            "message": "Password Updated Successfully!"
        },
        "data": {}
    }
}
```

### Remarks


#  CHANGE USER PASSWORD API

To get the Password create/update Condition

### Prerequisites
There is no Prerequistes for this API

### HTTP Request

```
/irrc/get_user_password_policy
```

### Request headers

|    Name    |       Value     |
|:-----------|:----------------|
|Content-Type|application/json|
|TOKEN|aqsw3sakskwj32kj3k2j33j2j3k23kj2k3j|

### Request body

| Parameter | Type |           Description     |
|:----------|:-----|:--------------------------|
|min_password_length|Integer|Minimum Password length|
|password_lower_required|Boolean|To set lower case validation for password creation|
|password_upper_required|Boolean|To set upper case validation for password creation|
|password_numeric_required|Boolean|To set numeric value validation for password creation|
|password_special_required|Boolean|To set special character validation for password creation|

OR 

Pass Empty Json : { "params":{}"}


### Example

##### Request

```
{
  "params": {
  }
}
```
OR
```
{
  "params": {
    "min_password_length": 2,
    "password_lower_required": false,
    "password_upper_required": false,
    "password_numeric_required": false,
    "password_special_required": false
  }
}
```

##### Response

```
{
    "jsonrpc": "2.0",
    "id": null,
    "result": {
        "meta": {
            "status": true,
            "message": ""
        },
        "data": {
            "user_password_policy": [
                {
                    "min_password_length": 2,
                    "password_lower_required": false,
                    "password_upper_required": false,
                    "password_numeric_required": false,
                    "password_special_required": false
                }
            ]
        }
    }
}
```

### Remarks

# Authentication API

To Login Account and generate token

### Prerequisites

One of the following scopes are required to execute this request:

{{#foreach Request.Scopes}}
* {{Name}}
{{/foreach}}

### HTTP Request

```
/irrc/login
```
### Request parameters

In the request URL, provide the following query parameters with values.

| Parameter | Type | Description |
|:----------|:-----|:------------|


### Optional request headers

| Name | Value |
|:-----|:------|

### Request body

| Parameter | Type | Description |
|:----------|:-----|:------------|

### Example

##### Request

```http
```

##### Response

```http
```

### Remarks
