# Web Requests

All about curl.

#### 1.1 Hypertext Transfer Protocol (HTTP)

- Port 80 - default HTTP Port
- cURL - client URL
	- print raw HTML	
		- `$ curl (URL)`
	- get HTML file
		- `$ curl -O (URL)`
	- silence output (`-s` flag)

#### 1.2 Hypertext Transfer Protocol Secure (HTTPS)

- Clear-text DNS servers can expose data on HTTPS
	- Use encrypted DNS or a VPN to ensure proper encryption
- Invalid or outdated SSL certificate allows for MITM attacks
	- For testing or practice purposes, use the `-k` flag to ignore SSL certs

#### 1.3 HTTP Requests and Responses

- HTTP version 1.X sends as clear-text
- HTTP version 2.X sends as binary in dictionary form
- Get verbose response
	- `$ curl (URL) -v`
- Very verbose response `(REALLY COOL)`
	- `$ curl (URL) -vvv`

#### 1.4 HTTP Headers

- General headers
	- describe the message
- Entity headers
	- describe the content
- Request headers
	- don't describe the content
- Response headers
	- don't describe the content
- Security headers
	- describe certain rules and policies
- Show only the headers
	- `$ curl (URL) -I`
- Change headers with `-H` flag
- Change user-agent
	- `$ curl (URL) -A (agent string)`
- Find headers under Inspect > Network > (file name) > Headers

#### 2.1 HTTP Methods and Codes

- Common methods
	- GET - requests a specific resource
	- POST - sends data to the server
	- HEAD
	- PUT
	- DELETE
	- OPTIONS
	- PATCH
- Common status codes
	- 200 Ok
	- 302 Found - redirects client to another URL
	- 400 Bad Request
	- 403 Forbidden - client does not have permission
	- 404 Not Found
	- 500 Internal Server Error - server can't process request

#### 2.2 GET

- Target Machine - `154.57.164.78:31070`
- Credentials can be sent over `basic HTTP auth` instead of `GET` or `POST`
	- This directly interacts with the server, bypassing the webpage
- Authenticate over curl
	- `$ curl admin:admin@154.57.164.78:31070 -v`
- Decode base64 (found under Authorization header of type `basic`)
	- `$ echo YWRtaW46YWRtaW4= | base64 -d`
- Spoof authentication via header change
	- `$ curl 154.57.164.78:31070 -H 'Authorization: Basic YWRtaW46YWRtaW4=' -v`
- Copy request for terminal
	- In browser inspector under network, select request and `Copy > Copy as cURL`
- Copy request for browser
	- `Copy > Copy as Fetch`
	- Paste into inspector console

#### 2.3 POST

- Target Machine - `154.57.164.83:32444`
- Why POST over GET
	- Lack of logging (inefficient to log)
	- Fewer encoding requirements (URLs need readable chars)
	- More data can be sent (no URL length limits)
- Investigate the POST request in Inspect > Network
	- Request tab > Raw
	- `username=admin&password=admin`
- Spoof POST authentication
	- `$ curl -X POST -d 'username=admin&password=admin' http://154.57.164.83:32444/`
	- If next page is different from auth page, include `-L` flag
- Use `Set-Cookie` header value to persist auth
	- `$ curl -b 'PHPSESSID=0bdes67g5hlq48dccit8jjlf5h' 154.57.164.83:32444`
	- or
	- `$ curl -H 'Cookie: PHPSESSID=0bdes67g5hlq48dccit8jjlf5h' 154.57.164.83:32444`
- Via inspector
	- Storage > Cookies > Delete Cookie if exist
	- Add with plus button
	- Name: `PHPSESSID`
	- Value: `0bdes67g5hlq48dccit8jjlf5h`
	- Reload
- Confirm content type from request headers and perform search from the terminal
	- `$ curl -X POST -d '{"search":"seattle"}' -b 'PHPSESSID=0bdes67g5hlq48dccit8jjlf5h' -H 'Content-Type: application/json' 154.57.164.83:32444/search.php`

#### 2.4 CRUD API
