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
```
from http.server import HTTPServer,BaseHTTPRequestHandler

content='''
<!doctype html>
<html>
<head>
<title> My Web Server</title>
</head>
<body>
<h1>Top Five Web Application Development Frameworks</h1>
<h2>1.Django</h2>
<h2>2. MEAN Stack</h2>
<h2>3. React </h2>
</body>
</html>
'''

class MyServer(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Get request received...")
        self.send_response(200) 
        self.send_header("content-type", "text/html")       
        self.end_headers()
        self.wfile.write(content.encode())

print("This is my webserver") 
server_address =('',8000)
httpd = HTTPServer(server_address,MyServer)
httpd.serve_forever()
```

## OUTPUT:

## CLIENT OUTPUT:
![Screenshot 2023-04-03 083947](https://user-images.githubusercontent.com/119406959/229402918-aa470c32-f204-44d3-b371-74e031e19804.png)

 ##SERVER OUTPUT:
 ![WhatsApp Image 2023-04-03 at 8 39 20 AM](https://user-images.githubusercontent.com/119406959/229403073-5a3dc993-1c9f-4ade-9839-93d99850ebde.jpeg)


## RESULT:
The program is executed succesfully
