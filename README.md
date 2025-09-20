# EX01 Developing a Simple Webserver

# Date:19-09-2025
# AIM:
To develop a simple webserver to serve html pages and display the configuration details of laptop.

# DESIGN STEPS:
## Step 1:
HTML content creation.

## Step 2:
Design of webserver workflow.

## Step 3:
Implementation using Python code.

## Step 4:
Serving the HTML pages.

## Step 5:
Testing the webserver.

# PROGRAM:
```from http.server import HTTPServer,BaseHTTPRequestHandler
content='''<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <titl></title>
</head>
<body align="center" bgcolor="aqua">
    <h1><u>TCP/IP Protocol</u></h1>
     <h2><i>
     1. Appliction layer</i></h2>
     <h2><i>2. Transport layer</i></h2>
     <h2><i>3. Internet layer</i></h2>
     <h2><i>4. Network access layer</i></h2>
     
</body>
</html>'''
class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get requesst received...")
        self.send_response(200)
        self.send_header("content-type","text/html")
        self.end_headers()
        self.wfile.write(content.encode())
print("This is  my webserver")
server_address=('',8000)
httpd=HTTPServer(server_address,MyServer)
httpd.serve_forever()
```
# OUTPUT:
![alt text](<Screenshot 2025-09-20 113816.png>)
![alt text](<Screenshot 2025-09-19 130155.png>)
# RESULT:
The program for implementing simple webserver is executed successfully.
