# SMS Messaging API
***

## API Document

### Endpoint (ENDPOINT)
`https://api.example-domain.com`

### Request

#### Method
`POST`

#### URL
`{{ENDPOINT}}/message-in`

#### Headers
```
{
    'Content-Type': 'application/json',
    'Accept': 'application/json'
}
```
#### Body
```
{
    'key' : 'api incoming key for checking is verified',
    'title' : 'message title',
    'body' : 'message body'
}
```

### Response

#### Body
```
{
    'status' : '200',
    'message' : 'success'
}
```

#### Status list
```
{
    '200' : 'success', // all process is completed
    '100' : 'invalid parameters', // missing parameter or wrong parameter format
    '300' : 'invalid key', // wrong key or key is not verified
    '500' : 'internal server error' // API error, Please contact support team
}
```
