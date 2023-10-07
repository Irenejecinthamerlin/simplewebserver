# EX01 Developing a Simple Webserver
# Date: 20/09/2023

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
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1>Top 5 Revenue Generating Companies<h1>
<UL TYPE=“circle”>
<LI> Accenture </LI>		
<LI> Amazon </LI>
<LI> Cognizant Technology Solutions </LI>
<LI> HCLTech </LI>
<LI> Vitol </LI>
</UL>
</body>
</html>
"""
```
## README.md
```
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

![image](https://github.com/Irenejecinthamerlin/simplewebserver/assets/128350225/29f6d616-fa57-49c4-93be-66b93bc47d5f)


![image](https://github.com/Irenejecinthamerlin/simplewebserver/assets/128350225/6dd9df4b-0de6-4b1f-9eb9-735d57894b7a)



## RESULT:
The program for implementing simple webserver is executed successfully.
