¡Entendido! Vamos a hacer un "reset" completo. He extraído la estructura exacta y cada ejemplo de la referencia que mencionas, traduciendo las explicaciones al español pero manteniendo la precisión técnica que un Senior espera de su documentación.

Aquí tienes la **Python Cheat Sheet** definitiva, estructurada punto por punto como en `quickref.me`.

---

# 🐍 Referencia Rápida de Python (QuickRef)

## 📑 Tabla de Contenidos

* [Getting Started](#getting-started)
* [Python Built-in Data Types](#python-built-in-data-types)
* [Python Advanced Data Types](#python-advanced-data-types)
* [Python Strings](#python-strings)
* [Python F-Strings (Since Python 3.6+)](#python-f-strings-since-python-36)
* [Python Lists](#python-lists)
* [Python Flow control](#python-flow-control)
* [Python Loops](#python-loops)
* [Python Functions](#python-functions)
* [Python Modules](#python-modules)
* [Python File Handling](#python-file-handling)
* [Python Classes & Inheritance](#python-classes--inheritance)
* [Miscellaneous](#miscellaneous)

---

## Getting Started

### Hola Mundo

```python
print("¡Hola, Mundo!")

```

### Comentarios

```python
# Este es un comentario de una sola línea

""" Este es un comentario
    multilínea en Python
"""

```

### Variables

```python
nombre = "Juan"   # Cadena (str)
edad = 25         # Entero (int)
altura = 1.75     # Flotante (float)
es_estudiante = True # Booleano (bool)

```

---

## Python Built-in Data Types

| Tipo | Descripción | Ejemplo |
| --- | --- | --- |
| `str` | Texto | `"Hola"`, `'Mundo'` |
| `int` | Enteros | `1`, `100`, `-5` |
| `float` | Decimales | `3.14`, `2.0` |
| `bool` | Lógicos | `True`, `False` |
| `NoneType` | Nulo | `None` |

---

## Python Advanced Data Types

### Listas (Lists)

Colección ordenada y mutable.

```python
nums = [1, 2, 3]

```

### Tuplas (Tuples)

Colección ordenada e inmutable.

```python
punto = (10, 20)

```

### Diccionarios (Dictionaries)

Colección de pares clave-valor.

```python
persona = {"nombre": "Ana", "edad": 30}

```

### Conjuntos (Sets)

Colección desordenada de elementos únicos.

```python
colores = {"rojo", "verde", "azul"}

```

---

## Python Strings

### Cadenas multilínea

```python
mensaje = """Hola,
esto es una cadena
de varias líneas."""

```

### Métodos de cadena

```python
s = "  Hola Mundo  "
print(s.upper())      # "  HOLA MUNDO  "
print(s.lower())      # "  hola mundo  "
print(s.strip())      # "Hola Mundo" (quita espacios)
print(s.replace("H", "J")) # "Jola Mundo"
print(s.split(" "))   # ['', '', 'Hola', 'Mundo', '', '']

```

### Slicing (Rebanado)

```python
s = "Python"
print(s[0:2])  # "Py" (del índice 0 al 2, excluyendo el 2)
print(s[:4])   # "Pyth"
print(s[2:])   # "thon"
print(s[-2:])  # "on"

```

---

## Python F-Strings (Since Python 3.6+)

### Sintaxis básica

```python
nombre = "Mundo"
print(f"Hola, {nombre}!") # "Hola, Mundo!"

```

### Expresiones y Formato

```python
val = 12.34567
print(f'{val:.2f}')  # "12.35" (redondeo a 2 decimales)
print(f'{10 * 2}')   # "20"

```

---

## Python Lists

### Acceso y modificación

```python
lista = ["a", "b", "c"]
print(lista[1])     # "b"
lista[1] = "z"      # ["a", "z", "c"]

```

### Métodos de lista

```python
lista.append("d")   # Añadir al final
lista.insert(1, "x")# Insertar en índice 1
lista.pop()         # Eliminar último elemento
lista.remove("a")   # Eliminar elemento específico
lista.sort()        # Ordenar lista

```

---

## Python Flow control

### Sentencias If

```python
x = 10
if x > 10:
    print("Mayor que 10")
elif x < 10:
    print("Menor que 10")
else:
    print("Es 10")

```

---

## Python Loops

### Bucle For

```python
for i in range(5):
    print(i) # Imprime de 0 a 4

frutas = ["manzana", "banana"]
for f in frutas:
    print(f)

```

### Bucle While

```python
i = 1
while i < 5:
    print(i)
    i += 1

```

### Break y Continue

```python
for i in range(10):
    if i == 3: continue # Salta al siguiente ciclo
    if i == 5: break    # Rompe el bucle
    print(i)

```

---

## Python Functions

### Definición y argumentos

```python
def mi_funcion(nombre, saludo="Hola"):
    return f"{saludo}, {nombre}"

print(mi_funcion("Alex"))             # "Hola, Alex"
print(mi_funcion("Maria", "Buenos días")) # "Buenos días, Maria"

```

### Funciones Lambda

```python
doble = lambda x: x * 2
print(doble(5)) # 10

```

---

## Python Modules

### Importación

```python
import math
print(math.sqrt(16)) # 4.0

from math import pi
print(pi) # 3.141592653589793

```

---

## Python File Handling

### Leer Archivos

```python
# Línea por línea
with open("myfile.txt") as file:
    for line in file:
        print(line)

# Con número de línea
file = open('myfile.txt', 'r')
for i, line in enumerate(file, start=1):
    print("Number %s: %s" % (i, line))

```
### Escribir y Manejar Objetos (JSON)

```python
import json

# Escribir String
contents = {"aa": 12, "bb": 21}
with open("myfile1.txt", "w+") as file:
    file.write(str(contents))

# Escribir Objeto (JSON)
with open("myfile2.txt", "w+") as file:
    file.write(json.dumps(contents))

# Leer Objeto (JSON)
with open("myfile2.txt", "r+") as file:
    contents = json.load(file)
    print(contents)

```

### Borrar Archivos y Carpetas
```python
import os

# Borrar archivo
os.remove("myfile.txt")

# Check y Borrar
if os.path.exists("myfile.txt"):
    os.remove("myfile.txt")
else:
    print("The file does not exist")

# Borrar Carpeta
os.rmdir("myfolder")

```

---

## Python Classes & Inheritance

### Clase básica

```python
class Persona:
    def __init__(self, nombre, edad):
        self.nombre = nombre
        self.edad = edad

    def saludar(self):
        print(f"Hola, soy {self.nombre}")

p1 = Persona("Carlos", 20)
p1.saludar()

```

### Herencia

```python
class Estudiante(Persona):
    def __init__(self, nombre, edad, grado):
        super().__init__(nombre, edad)
        self.grado = grado

e1 = Estudiante("Ana", 18, "Primero")
e1.saludar()

```

---

## Miscellaneous

### List Comprehension

```python
nums = [1, 2, 3, 4]
cuadrados = [n**2 for n in nums] # [1, 4, 9, 16]

```

### Operador Ternario

```python
edad = 20
estado = "Adulto" if edad >= 18 else "Menor"

```

---

¿Te gustaría que añada una sección extra de **Python Pro-Tips** con errores comunes que suelen cometer los Juniors al usar estas estructuras?
