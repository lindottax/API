

### /identity/users/password/confirm_code

#### POST
##### Description:

Sets new account password

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| reset_password_token | formData | Token from email | Yes | string |
| password | formData | User password | Yes | string |
| confirm_password | formData | User password | Yes | string |
| lang | formData | Language in iso-2 format | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Resets password |
| 400 | Required params are empty |
| 404 | Record is not found |
| 422 | Validation errors |

### /identity/users/password/generate_code

#### POST
##### Description:

Send password reset instructions

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| email | formData | Account email | Yes | string |
| lang | formData | Language in iso-2 format | No | string |
| captcha_response | formData | Response from captcha widget | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Generated password reset code |
| 400 | Required params are missing |
| 404 | User doesn't exist |
| 422 | Validation errors |



### /identity/sessions

#### DELETE
##### Description:

Destroy current session

##### Responses

| Code | Description |
| ---- | ----------- |
| 204 | Destroy current session |
| 400 | Required params are empty |
| 404 | Record is not found |

#### POST
##### Description:

Start a new session

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| email | formData |  | Yes | string |
| password | formData |  | Yes | string |
| captcha_response | formData | Response from captcha widget | No | string |
| otp_code | formData | Code from Google Authenticator | No | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Start a new session |
| 400 | Required params are empty |
| 404 | Record is not found |

### /identity/configs

#### GET
##### Description:

Get barong configurations

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Get barong configurations |

### /identity/version

#### GET
##### Description:

Get barong version

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Get barong version |

### /identity/time

#### GET
##### Description:

Get server current unix timestamp.

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Get server current unix timestamp. |

### /identity/ping

#### GET
##### Description:

Test connectivity

##### Responses

| Code | Description |
| ---- | ----------- |
| 200 | Test connectivity |

### /identity/password/validate

#### POST
##### Description:

Password strength testing

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| password | formData | User password | Yes | string |

##### Responses

| Code | Description |
| ---- | ----------- |
| 201 | Password strength testing |


