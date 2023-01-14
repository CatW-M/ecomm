# ecomm
1. Created repo on github, selecting Python dropdown for README.md
2. Cloned repo on local machine and navigated to the repo
3. Created django app by typing 

``` django-admin startproject ecomm . ```

The period at the end is to keep the readme and gitignore at the root level.

4. ``` python3 manage.py runserver ```
To check installation was successful. Control-C to exit and return to terminal.

5. ``` touch .env ```

6. If not already installed: ``` pip install python-decouple ```

7. Go to settings.py and add ``` from decouple import config ``` underneath ``` from pathlib import Path```

8. In the .env file created in step 5, add ```SECRET_KEY=<your SECRET_KEY from the settings.py> ```

9. In settings.py, replace your SECRET_KEY with ```SECRET_KEY = config("SECRET_KEY")```

(After this step, you can push your code to git, but don't do it before.)

10. Create primary app of our project ```django-admin startapp main_app``` (I've named it main_app which is pretty standard, but you can name it anything you want.)