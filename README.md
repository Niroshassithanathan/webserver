# Developing a Simple Webserver

# AIM:

To develop a simple webserver to serve html programming pages.

## DESIGN STEPS:

### Step 1:

HTML content creation is done

### Step 2:

Design of webserver workflow

### Step 3:

Implementation using Python code

### Step 4:

Serving the HTML pages.

### Step 5:

Testing the webserver

## PROGRAM:
# DEVELOPED BY NIROSHA 
# REG.NO : 212222230097
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """
<!DOCTYPE html>
<html>
<head>
<title>My webserver</title>
</head>
<body>
<h1><u>Languages used in Web.</u><h1>
<ul>
<li>Django</li>
<li>Angular or Angular JS</li>
<li>Laravel.</li>
<li>Meteor. </li>
<li>ASP.NET. </li>
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
server_address = ('',80)
httpd = HTTPServer(server_address,myhandler)
print("my webserver is running...")
httpd.serve_forever()
```
## OUTPUT:

![webO1](https://user-images.githubusercontent.com/121418437/229303593-49db537b-eb57-4914-aba7-b3e17ac61a18.PNG)

![webO2](https://user-images.githubusercontent.com/121418437/229303628-f08ecea6-f812-4bce-8ef1-0816c9501bd4.PNG)

## RESULT:

  The program is executed succesfully
