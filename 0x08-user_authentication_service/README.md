![](img-readme.png)


# Requirements

- Allowed editors: vi, vim, emacs
- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly #!/usr/bin/env python3
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5)
- All your files must be executable
- The length of your files will be tested using wc
- All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
- All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
- All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
- All your functions should be type annotated
- The flask app should only interact with Auth and never with DB directly.
- Only public methods of Auth and DB should be used outside these classes

## Task

**0. User model**
[user.py](user.py/) - [main.py](0-main.py/)

**1. create user**
File: [db.py](db.py) - [main.py](1-main.py/)

**2. Find user**
File: [db.py](db.py) - [main.py](2-main.py)

**3. update user**
File: [api/v1/auth/session_auth.py](api/v1/auth/session_auth.py/) - [main.py](3-main.py)

**4. Hash password**
File: [auth.py](auth.py/) - [main.py](4-main.py)

**5. Register user**
File: [auth.py](auth.py/) - [main.py](5-main.py/)

**6. Basic Flask app**
File: [app.py](app.py/)

**7. Register user**
File: [app.py](app.py/)

**8. Credentials validation**
Files: [auth.py](auth.py/) - [main.py](8-main.py/)

**9. Generate UUIDs**
File: [auth.py](auth.py/)

**10. Sessions in database**
File: [auth.py](auth.py/) - [main.py](10-main.py/)

**11. Log in**
File: [app.py](app.py/)

**12. Find user by session ID**
File: [auth.py](auth.py/)

**13. Destroy session**
File: [auth.py](auth.py/)

**14. Log out**
File: [app.py](app.py/)

**15. User profile**
File: [app.py](app.py/)

**16. Generate reset password token**
File: [auth.py](auth.py/)

**17. Get reset password token**
File: [app.py](app.py/)

**18. Update password**
File: [auth.py](auth.py/)

**19. End-to-end integration test**
File: [app.py](app.py/)

**20. End-to-end integration test**
File: [main.py](main.py/)
