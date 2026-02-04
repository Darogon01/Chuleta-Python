


---

# 🐍 Python Master Roadmap: De Junior a Senior

## 📑 Tabla de Contenidos

* [1. Core Python](#1.-core-python)
* [2. Built-in Data Structures](#2-built-in-data-structures)
* [3. Modular Code & I/O](#3-modular-code--io)
* [4. OOP (Object-Oriented Programming)](#4-oop-object-oriented-programming)
* [5. Intermediate Python](#5-intermediate-python)
* [6. Environments & Automation](#6-environments--automation)
* [7. Backend / Data Path](#7.-backend--data-path)
* [8. Production Level](#8-production-level)

---

## 01. Core Python

La base del lenguaje. Aquí aprendes las reglas del juego.

### Syntax & Semantics

Python usa la **indentación** para definir bloques. No hay llaves `{}`. Si fallas en el espacio, el código falla.

```python
def mi_bloque():
    # Todo lo que esté a 4 espacios pertenece a la función
    if True:
        print("Indentación correcta")

```

### Variables & Data Types

Python es de **tipado dinámico**: no declaras el tipo, pero Python sabe qué es.

```python
edad = 25              # int: Números sin decimales
precio = 19.99         # float: Números con decimales
usuario = "DevJunior"  # str: Cadenas de texto
es_activo = True       # bool: Solo True o False

```

### Control Flow (if/elif/else)

```python
puntos = 85
if puntos >= 90:
    print("Excelente")
elif puntos >= 70:
    print("Aprobado")
else:
    print("Reprobado")

```

### Loops (for, while)

* **For**: Para iterar sobre una secuencia conocida.
* **While**: Para repetir mientras una condición sea cierta.

```python
# For loop
for i in range(3): # Itera 0, 1, 2
    print(f"Número: {i}")

# While loop
contador = 5
while contador > 0:
    print(contador)
    contador -= 1

```

### Functions (def, return)

```python
def sumar(a: int, b: int) -> int: # '-> int' es una pista de que devuelve un entero
    """Documentación: Suma dos números y devuelve el resultado."""
    return a + b

resultado = sumar(5, 10)

```

---

## 02. Built-in Data Structures

Cómo manejar colecciones de datos.

### List, Tuple, Set, Dict

| Estructura | Sintaxis | Característica |
| --- | --- | --- |
| **List** | `[1, 2]` | Ordenada y mutable (puedes cambiarla). |
| **Tuple** | `(1, 2)` | Inmutable (no cambia, es más rápida). |
| **Set** | `{1, 2}` | Sin orden, **sin duplicados**. |
| **Dict** | `{"k": "v"}` | Par Clave-Valor. |

### CRUD Operations

```python
frutas = ["manzana"]
frutas.append("pera")     # Create
print(frutas[0])          # Read
frutas[0] = "naranja"     # Update
frutas.remove("naranja")  # Delete

```

### Comprehensions

Una forma rápida de crear listas o diccionarios.

```python
# Crear lista de cuadrados de números pares
cuadrados = [x**2 for x in range(10) if x % 2 == 0]

```

### Error Handling (try/except)

```python
try:
    numero = int("no_soy_un_numero")
except ValueError as e:
    print(f"Error de conversión: {e}")
finally:
    print("Esto se ejecuta siempre.")

```

---

## 03. Modular Code & I/O

Organiza tu código para que sea escalable.

### Modules & Packages / Imports

* **Módulo**: Un archivo `.py`.
* **Paquete**: Una carpeta con un archivo `__init__.py`.

```python
import math               # Importa todo el módulo
from os import path       # Importa solo una parte
import pandas as pd       # Importa con un alias

```

### Scope (local/global)

```python
x = "Global" # Vive fuera

def mi_func():
    x = "Local" # Solo vive dentro de esta función
    print(x)

```

### File I/O (Input/Output)

```python
# Usamos 'with' para cerrar el archivo automáticamente
with open("notas.txt", "w") as f:
    f.write("Aprender Python es clave.")

with open("notas.txt", "r") as f:
    print(f.read())

```

---

## 04. OOP (Object-Oriented Programming)

Programación orientada a objetos: modelar el mundo real.

### Classes & Objects / __init__

```python
class Robot:
    def __init__(self, nombre):
        self.nombre = nombre  # Atributo
        self.__energia = 100  # Encapsulación (Privado con __)

    def saludar(self):
        return f"Hola, soy {self.nombre}"

mi_bot = Robot("RX-8") # Instancia (Objeto)

```

### Inheritance & Polymorphism

```python
class RobotCocinero(Robot): # Herencia
    def saludar(self):      # Polimorfismo (Cambiamos el saludo)
        return "Hola, soy un chef robot."

```

### Dunder Methods

Métodos mágicos para que tus clases se comporten como tipos nativos.

```python
def __str__(self): # Lo que sale al hacer print(objeto)
    return f"Robot {self.nombre}"

```

---

## 05. Intermediate Python

Herramientas avanzadas para optimizar.

* **Lambdas**: `doblar = lambda x: x * 2`.
* **Generators (yield)**: Devuelven valores uno a uno sin cargar toda la lista en memoria.
```python
def generador_numeros():
    for i in range(1000000):
        yield i

```


* **Decorators**: Funciones que modifican a otras funciones.
```python
def aviso(func):
    def wrapper():
        print("Iniciando...")
        func()
    return wrapper

@aviso
def mi_tarea(): print("Tarea hecha")

```



---

## 06. Environments & Automation

El entorno de trabajo.

* **pip / venv**: `python -m venv .venv` crea tu entorno. `pip install requests` instala librerías.
* **Web Scraping**: `BeautifulSoup` para extraer datos de HTML.
* **API Consumption**:
```python
import requests
r = requests.get("https://pokeapi.co/api/v2/pokemon/pikachu")
print(r.json()["name"])

```



---

## 7. Backend / Data Path

Donde Python domina el mercado laboral.

* **Backend**: FastAPI, Flask o Django para crear servidores web.
* **Data Path**:
* `NumPy`: Cálculos matemáticos complejos.
* `Pandas`: Manejo de tablas de datos (DataFrames).


```python
import pandas as pd
df = pd.read_csv("datos.csv")
print(df.describe()) # Resumen estadístico

```



---

## 08. Production Level

Código listo para la vida real.

* **Testing (pytest)**:
```python
def test_suma():
    assert 1 + 1 == 2

```


* **Logging**: No uses `print` en servidores, usa el log.
```python
import logging
logging.warning("Algo no va bien...")

```


* **Clean Code**: Código legible, modular y con nombres de variables que un humano entienda.

---

> **Senior Tip**: No intentes aprenderte cada línea hoy. Elige un bloque (por ejemplo, el 02) y juégalo hasta que te sientas cómodo. El código se aprende rompiéndolo.

¿Te gustaría que cree un **mini-proyecto** que combine los puntos 01 al 04 para que practiques la base de golpe?
