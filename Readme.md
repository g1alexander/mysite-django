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
