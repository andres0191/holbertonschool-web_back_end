

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

**0. Et moi et moi et moi!**
[api/v1/app.py](api/v1/app.py/) - [api/v1/views/users.py](api/v1/views/users.py)

**1. Empty session**
File: [api/v1/auth/session_auth.py](api/v1/auth/session_auth.py/) - [api/v1/app.py](api/v1/app.py/)

**2. Create a session**
File: [api/v1/auth/session_auth.py](api/v1/auth/session_auth.py)

**3. User ID from Session ID**
File: [api/v1/auth/session_auth.py](api/v1/auth/session_auth.py/)

**4. Session cookie**
File: [api/v1/auth/auth.py](api/v1/auth/auth.py/)

**5. Before request**
File: [api/v1/app.py](api/v1/app.py/)

**6. Use Session ID for identifying a User**
File: [api/v1/auth/session_auth.py](api/v1/auth/session_auth.py/)

**7. New view for Session Authentication**
File: [api/v1/views/session_auth.py](api/v1/views/session_auth.py/) - [api/v1/views/__init__.py](api/v1/views/__init__.py/)


**8. Logout**
Update the class SessionAuth by adding a new method def destroy_session(self, request=None): that deletes the user session / logout:

- If the request is equal to None, return False
- If the request doesn’t contain the Session ID cookie, return False - you must use self.session_cookie(request)
- If the Session ID of the request is not linked to any User ID, return False - you must use self.user_id_for_session_id(...)
- Otherwise, delete in self.user_id_by_session_id the Session ID (as key of this dictionary) and return True

Update the file api/v1/views/session_auth.py, by adding a new route DELETE /api/v1/auth_session/logout:

- Slash tolerant
- You must use from api.v1.app import auth
- You must use auth.destroy_session(request) for deleting the Session ID contains in the request as cookie:
> - If destroy_session returns False, abort(404)
> - Otherwise, return an empty JSON dictionary with the status code 200

**9. Expiration?**
File: [api/v1/auth/session_exp_auth.py](api/v1/auth/session_exp_auth.py/) - [api/v1/app.py](api/v1/app.py/)

**10. Sessions in database**
File: [api/v1/auth/session_db_auth.py](api/v1/auth/session_db_auth.py/) - [api/v1/app.py, models/user_session.py](api/v1/app.py, models/user_session.py/)

**11. Basic - Overload current_user - and BOOM!**
File: [api/v1/auth/basic_auth.py](api/v1/auth/basic_auth.py/)