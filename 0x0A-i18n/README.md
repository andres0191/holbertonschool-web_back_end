# Requirements

- All your files will be interpreted/compiled on Ubuntu 18.04 LTS using python3 (version 3.7)
- All your files should end with a new line
- The first line of all your files should be exactly #!/usr/bin/env python3
- A README.md file, at the root of the folder of the project, is mandatory
- Your code should use the pycodestyle style (version 2.5)
- All your files must be executable
- All your modules should have a documentation (python3 -c 'print(__import__("my_module").__doc__)')
- All your classes should have a documentation (python3 -c 'print(__import__("my_module").MyClass.__doc__)')
- All your functions (inside and outside a class) should have a documentation (python3 -c 'print(__import__("my_module").my_function.__doc__)' and python3 -c 'print(__import__("my_module").MyClass.my_function.__doc__)')
- A documentation is not a simple word, it’s a real sentence explaining what’s the purpose of the module, class or method (the length of it will be verified)
- All your functions and coroutines must be type-annotated.


## Task

**0. Basic Flask app**
File: [0-app.py](0-app.py/) - [templates/0-index.html](templates/0-index.html/)

**1. Basic Babel setup**
File: [1-app.py](1-app.py/) - [templates/1-index.html](templates/1-index.html/)

**2. Get locale from request**
File: [2-app.py](2-app.py/) - [templates/2-index.html](templates/2-index.html/)

**3. Parametrize templates**
File: [3-app.py](3-app.py/) - [templates/3-index.html](templates/3-index.html/) - [babel.cfg](babel.cfg/) - [translations/en/LC_MESSAGES/messages.po](translations/en/LC_MESSAGES/messages.po/) - [translations/fr/LC_MESSAGES/messages.po](translations/fr/LC_MESSAGES/messages.po/) - [translations/en/LC_MESSAGES/messages.mo](translations/en/LC_MESSAGES/messages.mo/) - [translations/fr/LC_MESSAGES/messages.mo](translations/fr/LC_MESSAGES/messages.mo/)

**4. Force locale with URL parameter**
File: [4-app.py](4-app.py/) - [templates/4-index.html](templates/4-index.html/)

**5. Mock logging in**
File: [5-app.py](5-app.py/) - [templates/5-index.html](templates/5-index.html/)

**6. Use user locale**
File: [6-app.py](6-app.py/) - [templates/6-index.html](templates/6-index.html/)

**7. Infer appropriate time zone**
File: [7-app.py](7-app.py/) - [templates/7-index.html](templates/7-index.html/)

**8. Display the current time**
File: [app.py](app.py/) - [templates/index.html](templates/index.html/) - [translations/en/LC_MESSAGES/messages.po](translations/en/LC_MESSAGES/messages.po/) - [translations/fr/LC_MESSAGES/messages.po](translations/fr/LC_MESSAGES/messages.po/)