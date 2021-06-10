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

#### Parte 4

- el sistema de vistas generica permite abstraer los patrones comunes hasta el punto en que ni siquiera es necesario escribir código Python para escribir una aplicación. me agrda :)

#### Parte 5

- Hacer pruebas son muy importantes

  - Si quiere ganarse la vida como un programador de Django, ¡Usted debe ser bueno escribiendo pruebas!
  - Las pruebas ayudan a los equipos a trabajar en conjunto
  - Las pruebas hacen más atractivo su código
  - Las pruebas no solo identifican los problemas, los previenen
  - Las pruebas le ahorrarán tiempo

- Los nombres de los tests deben ser tan largos?
- que dice esta linea?
  ```py
    return now - datetime.timedelta(days=1) <= self.pub_date <= now
  ```
- los tests se hacen tsnto el servidor como el cliente
- el cliente de python **"shell"** es un aliado importante
  - Django proporciona una prueba Client para simular un usuario interactúando con el código al nivel de la vista (brutal!)

```txt
Pruebas adicionales¶
Este tutorial sólo presenta algunos de los temas fundamentales de las pruebas. Hay mucho más que usted puede hacer y una serie de herramientas muy útiles a su disposición para lograr algunas cosas muy interesantes.

Por ejemplo, aunque nuestras pruebas han tratado aquí algo de la lógica interna de un modelo y la forma en que nuestras vistas publican información, usted puede utilizar un framework «en el navegador» como Selenium para probar la forma en que su HTML en realidad se renderiza en un navegador. Estas herramientas le permiten comprobar no sólo el comportamiento de su código Django, sino también, por ejemplo, el de su JavaScript. ¡Es impresionante ver cómo las pruebas ejecutan un navegador y comienzan a interactuar con su sitio como si estuviese siendo operado por un humano! Django incluye LiveServerTestCase para facilitar la integración con herramientas como Selenium.


```

#### Parte 6

- todo el css y js que necesitemos en nuestra aplicacion va dentro de un directorio **"static/{nombre_aplicacion}"**
