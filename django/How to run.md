

Installing pipenv.  
Using `pipenv install django` inside the project file.

Tip: open any file in vscode using the command `code .`

“pipenv shell” to activate the virtual environment.

Run “django-admin” to see the list of commands.

```bash
django-admin startproject <name> .  
```

Afterwards just use:

```shell
python <project name> <commands>
```
  
To make life easier we will use vs code terminal, to configure it go to the Command Palette (Ctrl + Shift + P), type python interpreter (Python: Select Interpreter) then add the path to your environment, (`pipenv –venv)` and add `/bin/python` add the end for example: 

```path
/home/jibna/.local/share/virtualenvs/storefront-2wEtHFzj/bin/python
 ```

Then you can easily run the VS Code terminal ``Ctrl + \```

Tip: To collapse side window `Ctrl + B`

Apparently we dont use the sessions app when developing with django anymore.

Tip: `Ctrl + L`  to clear terminal windows

Timeskip…

I had the issue of sqlite not working, and switched to mysql, hopefully it works

I am using heidiDb as my dba manager, and instead of the library mysqlclient, I am using mysql-connect-python

Using [Mockaroo](https://www.mockaroo.com/) to create dummy data.