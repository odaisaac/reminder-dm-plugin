# Zuri Chat DM (Reminder API)

Connect With Us: `developer@zuri.chat`
Zuri Chat is an open source slack clone. However, it offers a lot more functionality via a plugin system where each room can be provided by a different plugin provider.
​
## **Authentication**
this API does not require any authentication for use, 

## **Errors**
When an error occurs, you will receive an error object. Most of these error objects contain an error code and an error description so that your applications can more efficiently identify the problem.
​
If you get a 4xx response code, then you can assume that there is a bad request from your end. In this case, 
check the [Standard Error Responses](#standard-error-responses) for more context.
​
5xx errors suggest a problem on server's end.
​
​
​
## API methods:
- POST

## End Points:
base url: https://dm.zuri.chat/docs/v1
### /reminder
- **Endpoint**: reminder
- **Method**: Post
- **Description**: This is used to remind a user about a message.
#### parameters: 
| Name | Data type |
|--------|-------------|
| message_id (required)| string |
| current_date (required) | list of strings |
| scheduled_date (required)| string |
| notes| string |

####  Body Request Format
- use the endpoint **https://dm.zuri.chat/api/v1/reminder**

```sh
{
"mesage_id": "33",
"current_date": "Tue, 22 Nov 2011 06:00:00 GMT",
"scheduled_date":"Tue, 22 Nov 2011 06:00:00 GMT"
}
```

##### Response:

```json
code: 201
 { 
     "status": 201,
 }
```

```json
Code: 400
 Description: Bad Request
{
  "status": 400,
  "message": ""
}
```

