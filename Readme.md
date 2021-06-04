# Primera App en Django

### Tutorial de la documentacion de [Django](https://docs.djangoproject.com/es/3.2/intro/tutorial01/)

**Impresiones:**

#### Parte 1

- Me ha sorprendido la velocidad del framework
- Esta es una aplicacion monolitica?
- "mysite" es el proyecto y "polls" es la aplicacion
- "manage.py" es como el "index.php"?

#### Parte 2

- Las aplicaciones Django son «conectables»: Usted puede utilizar una aplicación en diversos proyectos y puede distribuir aplicaciones porque ellas no necesitan estar atadas a una determinada instalación de Django.

- Nota:
  recuerde la guía de tres pasos para hacer cambios de modelo:

  - Cambie sus modelos (en models.py).
  - Ejecute el comando python manage.py makemigrations para crear migraciones para esos cambios
  - Ejecute el comando python manage.py migrate para aplicar esos cambios a la base de datos.

- no entendi muy bien

  ```python
  def was_published_recently(self):
        return self.pub_date >= timezone.now() - datetime.timedelta(days=1)
  ```

- la Api de los modelos no me quedo muy claro (un poco pesada de manejar)

#### Parte 3

- las aplicaciones de python se pueden modularizar, esto permite que puedas poder un modulo en cualquier proyecto que desees

- si queremos redirecionar a un 404 personalizado lo hacemos con **Http404** en **view.py**?

- cuando utilizamos **templates** en django debemos pone dentro de subcarpetas para no generar conflicto

- no entiendo muy bien la filosofia del acoplamiento en la parte de http404
