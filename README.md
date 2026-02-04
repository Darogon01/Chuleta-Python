

# 🐍 Python Professional Roadmap: The Master Guide

## 📑 Tabla de Contenidos

* [01. Core Python](#1-core-python)
* [02. Built-in Data Structures](#2-built-in-data-structures)
* [03. Modular Code & I/O](#3-modular-code--io)
* [04. OOP (Object-Oriented Programming)](#4-oop-object-oriented-programming)
* [05. Intermediate Python](#5-intermediate-python)
* [06. Environments & Automation](#6-environments--automation)
* [07. Backend & Data Path](#7-backend--data-path)
* [08. Production Level](#8-production-level)


## 01. Core Python

El cimiento de todo. Sin esto, el resto se cae.

* **Syntax & Semantics:** Python usa la indentación (4 espacios) para definir bloques. No hay llaves `{}`.
* **Variables & Data Types:**
```python
entero = 10          # int
decimal = 10.5       # float
texto = "Hola"       # str
booleano = True      # bool

```


* **Control Flow (if/elif/else):**
```python
if stock > 10:
    print("Suficiente")
elif stock > 0:
    print("Casi agotado")
else:
    print("Sin stock")

```


* **Loops (for, while):**
```python
for i in range(3): print(f"Vuelta {i}") # For: sabes el límite
while activo: activo = False            # While: depende de una condición

```


* **Functions (def, return):**
```python
def calcular_iva(precio: float) -> float:
    return precio * 0.21

```



---

## 02. Built-in Data Structures

Donde guardas la información de manera inteligente.

* **List, Tuple, Set, Dict:**
```python
lista = [1, 2, 2]     # Mutable, ordenada
tupla = (1, 2, 3)     # Inmutable (más rápida)
conjunto = {1, 2, 3}  # Únicos, sin orden
diccionario = {"id": 1} # Clave-Valor (Búsqueda ultra rápida)

```


* **CRUD Operations:** Crear, Leer, Actualizar, Borrar.
```python
items = []
items.append("nuevo") # Create
val = items[0]        # Read
items[0] = "editado"  # Update
items.pop(0)          # Delete

```


* **Comprehensions:** Crear listas de forma elegante.
```python
dobles = [x * 2 for x in range(5)]

```


* **Error Handling (try/except):**
```python
try:
    f = 10 / 0
except ZeroDivisionError as e:
    print(f"Error capturado: {e}")

```



---

## 03. Modular Code & I/O

Cómo organizar tu proyecto para que no sea un caos.

* **Modules & Packages:** Un archivo `.py` es un módulo. Una carpeta con archivos `.py` es un paquete.
* **Imports (import, from):**
```python
import math
from os import path

```


* **Scope (local/global):** Lo que vive dentro de una función no existe fuera, a menos que uses `global` (evítalo si puedes).
* **File I/O:** Manejo de archivos.
```python
with open("config.txt", "r") as f: # 'with' asegura que el archivo se cierre solo
    contenido = f.read()

```


* **Code Organization:** Separar la lógica de negocio de la interfaz de usuario.

---

## 04. OOP (Object-Oriented Programming)

Programación para adultos. Modelar la realidad.

* **Classes & Objects:** La clase es el molde, el objeto es la galleta.
* **__init__:** El constructor que se ejecuta al crear el objeto.
* **Encapsulation:** Usar `_` o `__` para proteger datos internos.
* **Inheritance:** Heredar propiedades de otra clase.
* **Polymorphism:** Un método que se comporta distinto en diferentes clases.
* **Dunder Methods:**
```python
def __str__(self): return "Soy un objeto legible"

```



---

## 05. Intermediate Python

Trucos de "mago" para optimizar código.

* **Lambdas:** Funciones anónimas de una sola línea: `suma = lambda x, y: x + y`.
* **Iterators & Generators (yield):**
```python
def contador():
    yield 1 # No gasta RAM, devuelve el valor y "pausa" la función
    yield 2

```


* **Decorators (@decorator):** Envolver una función para añadirle lógica (ej: medir tiempo).
* **Regex (re):** Buscar patrones complejos en textos (ej: validar un email).

---

## 06. Environments & Automation

Tu kit de herramientas fuera del código.

* **pip, venv, poetry:**
* `pip`: Instala paquetes.
* `venv`: Crea un entorno aislado (tu "caja de arena").
* `poetry`: Manejo moderno de dependencias.


* **Dependency Management:** Archivos `requirements.txt` para que otros puedan instalar lo mismo que tú.
* **Web Scraping (BeautifulSoup, Scrapy):** Extraer datos de páginas web.
* **API Consumption (requests):** Hablar con otros servidores.

---

## 07. Backend / Data Path

Donde Python brilla en el mundo real.

* **Web Frameworks (Flask, Django, FastAPI):** Para crear servidores. FastAPI es el estándar actual por velocidad.
* **REST APIs:** Comunicación estándar mediante JSON.
* **ORMs & Databases:** Usar Python para escribir en SQL (ej: SQLAlchemy).
* **Data Path (NumPy, Pandas):** Análisis de datos masivos y tablas.
* **ML Basics:** Uso de `scikit-learn` para predicciones básicas.

---

## 08. Production Level

Lo que separa a un Junior de un Senior.

* **Testing (pytest):** Si no hay tests, no sabemos si funciona.
* **Logging:** Registrar qué pasa en el servidor (no uses `print` en producción).
* **Clean Code:** Seguir las reglas de PEP 8 (legibilidad).
* **Security:** No guardar contraseñas en el código, usar variables de entorno.
* **CI/CD:** Automatizar que el código se suba a la nube solo si los tests pasan.

---

### 💡 Último consejo de Senior

No intentes memorizar esto. Úsalo como un índice. Cuando necesites hacer un **Generator**, ven aquí, mira la palabra clave `yield` y busca la documentación oficial. La clave es saber que la herramienta existe.

¿Te gustaría que cree un **repositorio de ejemplo** con la estructura de carpetas real que debería tener un proyecto que cubra estos 8 puntos?
