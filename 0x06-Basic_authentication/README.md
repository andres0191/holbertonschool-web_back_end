![](img-readme.png)


# Requirements

## General

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly #!/usr/bin/env python3
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5.*)
- The length of your files will be tested using wc
- All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
- All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
- All your functions should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)

## Task

**0. Simple-basic-API**
In this archive, you will find a simple API with one model: User. Storage of these users is done via a serialization/deserialization in files.

## Setup and start server
```sh
bob@dylan:~$ pip3 install -r requirements.txt
...
bob@dylan:~$
bob@dylan:~$ API_HOST=0.0.0.0 API_PORT=5000 python3 -m api.v1.app
 * Serving Flask app "app" (lazy loading)
...
bob@dylan:~$
```

## Use the API (in another tab or in your browser)
```sh
bob@dylan:~$ curl "http://0.0.0.0:5000/api/v1/status" -vvv
*   Trying 0.0.0.0...
* TCP_NODELAY set
* Connected to 0.0.0.0 (127.0.0.1) port 5000 (#0)
> GET /api/v1/status HTTP/1.1
> Host: 0.0.0.0:5000
> User-Agent: curl/7.54.0
> Accept: */*
> 
* HTTP 1.0, assume close after body
< HTTP/1.0 200 OK
< Content-Type: application/json
< Content-Length: 16
< Access-Control-Allow-Origin: *
< Server: Werkzeug/1.0.1 Python/3.7.5
< Date: Mon, 18 May 2020 20:29:21 GMT
< 
{"status":"OK"}
* Closing connection 0
bob@dylan:~$
```


**1. Error handler: Unauthorized**
File: [api/v1/app.py](api/v1/app.py/) - [api/v1/views/index.py](api/v1/views/index.py/)

**2. Error handler: Forbidden**
File: [api/v1/app.py](api/v1/app.py/) - [api/v1/views/index.py](api/v1/views/index.py/)

**3. Auth class**
File: [api/v1/auth](api/v1/auth/) - [api/v1/auth/__init__.py](api/v1/auth/__init__.py/) - [api/v1/auth/auth.py](api/v1/auth/auth.py/)

**4. Define which routes don't need authentication**
File: [api/v1/auth/auth.py](api/v1/auth/auth.py/)

**5. Request validation!**
File: [api/v1/app.py](api/v1/app.py/) - [api/v1/auth/auth.py](api/v1/auth/auth.py/)

**6. Basic auth**
File: [api/v1/app.py](api/v1/app.py/) - [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**7. Basic - Base64 part**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**8. Basic - Base64 decode**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**9. Basic - User credentials**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**10. Basic - User object**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**11. Basic - Overload current_user - and BOOM!**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**12. Basic - Allow password with ":"**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)

**13. Require auth with stars**
File: [api/v1/auth/auth.py](api/v1/auth/auth.py/)