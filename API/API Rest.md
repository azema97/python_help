# API Rest

Una API REST (Representational State Transfer) es un conjunto de reglas que permiten la comunicación entre diferentes sistemas a través de HTTP, usualmente en la web. Estas APIs son diseñadas para ser simples y escalables.

Características principales de una API REST:
- **Stateless**: Cada petición del cliente al servidor debe contener toda la información necesaria para entender y procesar la solicitud.
- **Caché**: Las respuestas deben ser marcadas como cachéable o no para mejorar el rendimiento.
- **Cliente-Servidor**: La arquitectura se divide en clientes y servidores, lo que permite que ambos evolucionen independientemente.
- **Interfaz Uniforme**: Usa métodos HTTP estándar como GET, POST, PUT y DELETE para realizar operaciones.

---

### API Rest con Flask (Python)

```python
from flask import Flask, jsonify, request

app = Flask(__name__)

# Datos simulados
jugadores = [
    {'id': 1, 'nombre': 'Lionel Messi', 'equipo': 'PSG'},
    {'id': 2, 'nombre': 'Cristiano Ronaldo', 'equipo': 'Manchester United'}
]

@app.route('/jugadores', methods=['GET'])
def obtener_jugadores():
    return jsonify(jugadores)

@app.route('/jugadores', methods=['POST'])
def agregar_jugador():
    nuevo_jugador = request.get_json()
    jugadores.append(nuevo_jugador)
    return jsonify(nuevo_jugador), 201

@app.route('/jugadores/<int:id>', methods=['DELETE'])
def eliminar_jugador(id):
    jugador = next((j for j in jugadores if j['id'] == id), None)
    if jugador:
        jugadores.remove(jugador)
        return jsonify({'mensaje': 'Jugador eliminado'})
    return jsonify({'mensaje': 'Jugador no encontrado'}), 404

if __name__ == '__main__':
    app.run(debug=True)
```
