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
    <style>
        body{
            background-image: linear-gradient(15.875deg,aqua,red,yellow,green)
        }
    </style>
</head>
<body align="center">
    <h1><u>{TCP  /  IP} Protocol</u></h1>
     
    <ol type='1' start='1'>
    <h2>(A) Application layer</h1>
    <li><i>Provides services for user applications (web, email, file transfer).
    Protocols: HTTP, HTTPS, FTP, SMTP, DNS, POP3, IMAP</li>
    <h2>(B) Transport layer</h1>
    <li>Responsible for end-to-end communication between devices.
    TCP (Transmission Control Protocol): Reliable, connection-oriented (e.g., web, email).
    UDP (User Datagram Protocol): Fast, connectionless (e.g., streaming, gaming).</li>
    <h2><i>(C) Internet layer</h1>
    <li>Handles logical addressing and routing of data packets.
    Protocols: IP (IPv4/IPv6), ICMP, ARP</li>
    <h2><i>(D) Network access layer</h1>
    <li>Defines how data is physically sent over the network (hardware-level communication).
    Protocols: Ethernet, Wi-Fi, PPP</li>     
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
