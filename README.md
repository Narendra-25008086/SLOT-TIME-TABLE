# Ex03 Time Table
## Date:10-10-2025

## AIM
To write a html webpage page to display your slot timetable.

## ALGORITHM
### STEP 1
Create a Django-admin Interface.

### STEP 2
Create a static folder and inert HTML code.

### STEP 3
Create a simple table using ```<table>``` tag in html.

### STEP 4
Add header row using ```<th>``` tag.

### STEP 5
Add your timetable using ```<td>``` tag.

### STEP 6
Execute the program using runserver command.

## PROGRAM
```
from http.server import HTTPServer, BaseHTTPRequestHandler

content = """
<!DOCTYPE html>
<html>
    <body>
    <center>
        <h1><u>SLOT TIME TABLE-(NKK)</u></h1>
    </center>
        <table border ="5" cellpadding="5" cellspacing="5" align="center">
            <tr bgcolor="blue">
                <th>Day/Time</th>
                <th>Monday</th>
                <th>Tuesday</th>
                <th>Wednesday</th>
                <th>Thursday</th>
                <th>Friday</th>
                <th>Saturday</th>
            </tr>
            <tr bgcolor="green">
                <th bgcolor="blue">8-10 </th>
                <td>FREE</td>
                <td>FREE</td>
                <td>FWAD</td>
                <td>ITDS</td>
                <td>FREE</td>
                <td>FREE</td>
            </tr>
            <tr bgcolor="green">
                <th bgcolor="blue">10-12</th>
                <td>PYTHON</td>
                <td>ITDS</td>
                <td>FWAD</td>
                <td>PYTHON</td>
                <td>ITDS</td>
                <td>FREE</td>
            </tr>
            <tr bgcolor="green">
                <th bgcolor="blue">12-1</th>
                <th cOlspan="7">LUNCH</th>
            </tr>
            <tr bgcolor="green">
                <th bgcolor="blue">1-3</th>
                <td>FREE</td>
                <td>ITDS</td>
                <td>FREE</td>
                <td>FWAD</td>
                <td>ITDS</td>
                <td>FREE</td>
            </tr>
            <tr bgcolor="green">
                <th bgcolor="blue">3-5</th>
                <td>FREE</td>
                <td>FWAD</td>
                <td>PYTHON</td>
                <td>PYTHON</td>
                <td>PYTHON</td>
                <td>FWAD</td>
            </tr>
        </table>
        <center><h1 ><u>SUBJECT DETAILS</u></h1></center>
        
        <table border="2" cellpadding="5" align="center">
            <tr bgcolor="yellow">
                <th>S.No.</th>
                <th>Subject Code</th>
                <th>Subject Name</th>
            </tr>
            <tr bgcolor="lightcyan">
                <td>1.</td>
                <td>19AI414</td>
                <td>Fundamentals of Web Application Development(FWAD)</td>
            </tr>
            <tr bgcolor="lightcyan">
                <td>2.</td>
                <td>19AI301</td>
                <td>Python Programming(PYTHON)</td>
            </tr>
            <tr bgcolor="lightcyan">
                <td>3.</td>
                <td>19AI403</td>
                <td>INTRODUCTION TO DATA SCIENCE</td>
            </tr>
        </table>
    </body>
</html>
"""

class MyHandler(BaseHTTPRequestHandler):
    def do_GET(self):
        print("Request received from:", self.client_address)
        self.send_response(200)
        self.send_header('Content-type', 'text/html; charset=utf-8')
        self.end_headers()
        self.wfile.write(content.encode('utf-8'))

server_address = ('', 8000)
httpd = HTTPServer(server_address, MyHandler)
print("My webserver is running on http://localhost:8000 ...")
httpd.serve_forever()
```



## OUTPUT


## RESULT
The program for creating slot timetable using basic HTML tags is executed successfully.
