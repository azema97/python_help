# ¿Que es Flask?

Flask es un microframework de Python que te permite construir aplicaciones web de manera rápida y sencilla. Es ligero y se centra en ofrecerte las herramientas básicas necesarias para crear una web app, sin muchas configuraciones complicadas o una estructura rígida. Ideal para proyectos pequeños y medianos, donde necesitas algo funcional sin complicarte demasiado.

- [Crea Un API Con Python En 10 minutos](https://youtu.be/b0ZrmhyyCY4?feature=shared)

Aquí tienes un ejemplo básico para crear una pequeña aplicación web con Flask:

```python
from flask import Flask

app = Flask(__name__)

@app.route('/')
def home():
    return "¡Hola, Mundo!"

if __name__ == '__main__':
    app.run(debug=True)
```

1. Se importa la clase `Flask` del paquete `flask`.
2. Se crea una instancia de `Flask`.
3. Se define una ruta con la función `@app.route('/')`, que define el punto de entrada a la web app (en este caso, la página principal).
4. La función `home()` devuelve un mensaje simple.
5. Finalmente, se ejecuta la aplicación en modo de depuración con `app.run(debug=True)`.