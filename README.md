

# 🐍 Python Professional Cheat Sheet (Senior Edition)

Guía de referencia rápida con navegación interna.

## 📑 Tabla de Contenidos

* [1. Variables y Constantes](#Variables-y-Constantes)
* [2. Datos Primitivos](#Datos-Primitivos)
* [3. Estructuras de Control (Ifs y Bucles)](#Estructuras-de-Control)
* [4. Funciones (Estructura Completa)](·funciones-estructura-completa)
* [5. Clases y POO](#clases-y-poo)
* [6. Equivalencias Functional JS (Map/Filter)](#equivalencias-functional-js-mapfilter)



## 1. Variables y Constantes

En Python no declaramos con `let` o `const`, el contexto lo da el nombre.

* **Variables:** `snake_case` (minúsculas).
* **Constantes:** `UPPER_CASE` (convención técnica).

```python
# Variable mutable
user_score = 150 

# Constante (Convención de solo lectura)
API_RETRY_LIMIT = 5 

```

---

## 2. Datos Primitivos

Los tipos de datos básicos del lenguaje.

| Tipo | Ejemplo | Explicación |
| --- | --- | --- |
| `int` | `x = 10` | Enteros. |
| `float` | `y = 10.5` | Decimales. |
| `str` | `s = "Dev"` | Cadenas de texto. |
| `bool` | `is_ready = True` | Lógicos (`True`/`False`). |
| `None` | `data = None` | El `null` de Python. |

---

## 3. Estructuras de Control (Ifs y Bucles)

Controlan el flujo lógico mediante la **indentación obligatoria**.

### Condicionales (If)

```python
if score >= 90:
    print("Senior")
elif score >= 50:
    print("Mid")
else:
    print("Junior")

```

### Bucles (Loops)

```python
# For: Iteración sobre rangos
for i in range(5): 
    print(f"Iteración {i}")

# While: Iteración por condición
while is_running:
    if error_detected:
        break # Rompe el bucle

```

---

## 4. Funciones (Estructura Completa)

Sintaxis con *Type Hinting* (Tipado para el IDE).

```python
def process_data(payload: dict, verbose: bool = False) -> bool:
    """
    Sintaxis: def nombre(param: tipo) -> retorno:
    """
    return True

# LLAMADA
status = process_data({"id": 1}, verbose=True)

```

---

## 5. Clases y POO

Estructura de objetos para arquitectura escalable.

```python
class DatabaseConnector:
    def __init__(self, connection_string: str):
        # Constructor
        self.uri = connection_string

    def connect(self):
        # Método
        print(f"Conectado a {self.uri}")

# INSTANCIACIÓN (Llamada a la clase)
db = DatabaseConnector("localhost:5432")
db.connect()

```

---

## 6. Equivalencias Functional JS (Map/Filter)

Traducción directa de métodos de Array de JS a Python.

* **Map (JS):** `arr.map(x => x * 2)`
* **Pythonic:** `[x * 2 for x in arr]`
* **Filter (JS):** `arr.filter(x => x > 10)`
* **Pythonic:** `[x for x in arr if x > 10]`

---

### 💡 Por qué tus enlaces fallaban:

GitHub genera los IDs de los encabezados de forma automática siguiendo estas reglas:

1. Pasa todo a **minúsculas**.
2. Quita signos de puntuación (puntos, paréntesis).
3. Cambia los **espacios por guiones `-**`.

Por eso, el enlace para `4. Funciones (Estructura Completa)` debe ser exactamente `#4-funciones-estructura-completa`.

¿Te gustaría que añada una sección sobre **Manejo de Errores (Try/Except)** o **Importación de módulos**?
