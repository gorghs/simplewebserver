# EX01 Developing a Simple Webserver
## Date: 26-11-2025

## Name: KARTHICK V
## REG NO: 212223040086
## AIM:
To develop a simple webserver to serve html pages and display the Device Specifications of your Laptop.

## DESIGN STEPS:
### Step 1: 
HTML content creation

### Step 2:
Design of webserver workflow.

### Step 3:
Implementation using Python code.

### Step 4:
Import the necessary modules.

### Step 5:
Define a custom request handler.

### Step 6:
Start an HTTP server on a specific port.

### Step 7:
Run the Python script to serve web pages.

### Step 8:
Serve the HTML pages.

### Step 9:
Start the server script and check for errors.

### Step 10:
Open a browser and navigate to http://127.0.0.1:8000 (or the assigned port).

## PROGRAM:
```
from http.server import HTTPServer, BaseHTTPRequestHandler
content = """

<html>
    <head>
       
    </head>
    <body>
        <h1 align="center"> Device Specification-25007799 </h1>
        <table border="4" align="center" >
            <tr>
                <th>S.NO.</th>
                <th>device specification</th>
                <th>details</th>
            </tr>
            <tr>
                <td>1</td>
                <td>Lenovo LOQ</td>
                <td>12 GB RAM , 512 GB SSD</td>
            </tr>
            <tr>
                <td>2</td>
                <td>acer</td>
                <td>16 GB RAM ,512 GB SSD</td>
            </tr>
            <tr>
                <td>3</td>
                <td>HP</td>
                <td>12 GB RAM,1 TB SDD</td>
            </tr>
            <tr>
                <td>4</td>
                <td>asus</td>
                <td>8 GB RAM,512 GB SSD</td>
            </tr>
            <tr>
                <td>5</td>
                <td>lenovo thinkpad</td>
                <td>12 GB RAM,512 GB SSD</td>
            </tr>
        </table>
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
<img width="1907" height="1054" alt="Screenshot 2025-09-27 164527" src="https://github.com/user-attachments/assets/bb3efd84-8fd4-4ace-a738-92edf84734ff" />
<img width="1870" height="1011" alt="Screenshot 2025-09-27 165205" src="https://github.com/user-attachments/assets/5473953c-92f5-4fdc-95b5-baa2513b0514" />




## RESULT:
The program for implementing simple webserver is executed successfully.
