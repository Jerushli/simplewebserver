# EX01 Developing a Simple Webserver
## Date:14-09-2023

## AIM:
To develop a simple webserver to serve html pages.

## DESIGN STEPS:
### Step 1: 
HTML content creation.

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Serving the HTML pages.

### Step 5:
Testing the webserver.

## PROGRAM:

```
Done by: JERUSHLIN JOSE
Reg NO : 212222240039

from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<!DOCTYPE html>
<html>
<head>
<title>Jeru's Webserver</title>
</head>

<body>
<h1>Top 5 revenue generating companies</h1>
<hr>
<h2>
<ol>
<li>Apple</li>
<li>Amazon</li>
<li>Microsoft</li>
<li>Infosys</li>
<li>Samsung</li>
</ol>
</h2>   

<h1>Done by Jerushlin jose JB(212222240039)

</body>
</html>

"""

class myhandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("request received")
        self.send_response(200)
        self.send_header('content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode())
server_address = ('',8000)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:

![image](https://github.com/Jerushli/simplewebserver/assets/120041243/3107d737-26f6-4d5d-b773-2aa6f239ebe7)



## RESULT:
The program for implementing simple webserver is executed successfully.
