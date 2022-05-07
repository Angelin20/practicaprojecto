# Django Admin LTE v3 theme

1. [Instale o virtualenvwrapper](https://virtualenvwrapper.readthedocs.io/en/latest/install.html)
2. Crear entorno virtual nuevo `python -m venv env`
3. Atualizar o pip: `pip install --upgrade pip`
4. Instalar paquetes `pip install -r requirements.txt`
5. Migrar datos de modelos predefinidos `python manage.py migrate`
7. Levantar servidor de desarrollo `python manage.py runserver 0.0.0.0:8000`
8. En caso de agregar nuevos modelos `python manage.py makemigrations`
9. Defina ipdb como default breackpoint `export PYTHONBREAKPOINT=ipdb.set_trace`
10. Crear un super usuario `python3 manage.py createsuperuser`

### Como generar una nueva version

1. En el archivo `setup.py`, incremente el numero de su version
2. En el archivo `setup.py`, si se creó una nueva carpeta en `templates` o en `estatic`, agregue estas carpetas usando las otras como ejemplo
3. Teste localmente:
    1. Cree la distro: `python setup.py sdist`
    2. Agregar el contenido en esta carpeta: `untar dist/django-theme-adminlte3-3.2.0.*`
    3. Vaciar los archivos innecesarios: `rm -rf dist django_theme_adminlte3.egg-info  django-theme-adminlte3-3.2.0.*`
4. Cree un tag con el mismo nombre de la `version` del archivo `setup.py`
5. Haga el push correspondiente sobre su tag
