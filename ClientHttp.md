# Generic client socket communication

Using HTTP 1.1 GET.

## Request

Method `GET` , URI path `/`.
URI query parameters:

- `cmd` = 3 digit integer, command id (format `%03d`)
- `json` = request data in JSON format (URL encoded)

### Example request

```http
GET /?cmd=005&json=%7B%22regid%22%3A%22rvg012345678%22%2C%22zone%22%3A13%2C%22url%22%3A%22server.revogi.com%22%2C%22port%22%3A5000%2C%22time%22%3A1729460140%7D HTTP/1.1
Cookie: JSESSIONID=A72F52D3D99B1D09CAF45C3EE27D85A6
User-Agent: Dalvik/2.1.0 (Linux; U; Android 15; Pixel 6 Pro Build/AP3A.241005.015)
Host: 192.168.0.1
Connection: Keep-Alive
Accept-Encoding: gzip
```

JSON payload:

```json
{
  "regid": "rvg012345678",
  "zone": 13,
  "url": "server.revogi.com",
  "port": 5000,
  "time": 1729460140
}
```

## Response

JSON data, containing:

- `response` = command id of the request this is a response to, number, no leading zeros
- `code` = HTTP status code (usually 200)
- optional `data` - contains actual response data


### Example response

To another request than above:

```http
HTTP/1.1 200 OK
Content-Length: 375
Content-Type:text/plain

{"response":2,"code":200,"data":{"signal":[{"ssid":"ssid_02","range":54,"security":5},{"ssid":"ssid_01","range":54,"security":5},{"ssid":"ssid_03","range":40,"security":5},{"ssid":"ssid_05","range":35,"security":5},{"ssid":"ssid_02","range":24,"security":5},{"ssid":"ssid_04","range":20,"security":7}]}}
```
