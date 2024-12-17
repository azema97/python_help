# ¿Que es un entorno virtual en Python?

Un entorno virtual en Python es un espacio aislado donde puedes instalar y gestionar librerías y dependencias de forma independiente del resto de tu sistema. Así, puedes trabajar en múltiples proyectos sin conflictos de versiones.

Beneficios:
- **Aislamiento**: Cada proyecto puede tener sus propias dependencias sin conflictos.
- **Facilita el despliegue**: Cuando pases de desarrollo a producción, el entorno será idéntico.
- **Manejo de versiones**: Puedes trabajar con versiones específicas de librerías y Python, sin afectar otros proyectos.
- **Seguridad**: Minimiza riesgos de afectar el entorno global y otros proyectos en tu máquina.

---

### Configurar un entorno virtual

Para configurar un entorno virtual nativamente en Python, sigue estos pasos:

1. Instala `virtualenv` (si aún no lo tienes):
```bash
pip install virtualenv
```

2. Crea un nuevo entorno virtual:
```bash
python -m virtualenv nombre_entorno

# Instalar sin las librerias globales
python -m venv --without-pip nombre_entorno
```

NOTA: Por protocolo, normalmente llamamos a los entornos como "env".

3. Activa el entorno virtual (Windows):

    - En Windows:
    ```bash
    .\nombre_entorno\Scripts\activate
    ```

    - En macOS y Linux:
    ```bash
    source nombre_entorno/bin/activate
    ```

4. Guardar dependencias en un archivo de texto llamado "requirements.txt":
```bash
pip freeze > requirements.txt
```

5. Desactiva el entorno (cuando ya no lo necesites):
```bash
deactivate
```

---

### Reutilizar requirements de un archivo de texto

Si tienes un archivo de requirements, puedes instalarlo en un entorno virtual con el siguiente comando:

```bash
pip install -r requirements.txt
```

Siendo `requirements.txt` el nombre del archivo, ubicándose en el mismo directorio (misma carpeta que el entorno).
