## El reto de una tortuga desde cero 🐢

## Que se busca

Implemetar funciones basicas de Python, en las cuales vamos a realizar una similación de nuestra tortuga. Se va a documentar la información sobre este proyecto y se explica la funcionalidad del mismo.


## Estructura generada en el proyecto.


```python
mini_turtle/
├── __init__.py           — exporta las funciones principales
├── draewer_logic.py      — lógica de dibujo
main.py                  — script principal de ejemplo
.gitignore               — archivos ignorados por git
LICENSE                  — licencia MIT
README.md                — este archivo

```

## Reto 1

**Simula el comportamiento de la tortuga usando solo print() e input().**

## Componentes principales

### 1. `mini_turtle/__init__.py`
**Qué es:** Archivo que convierte el directorio en un paquete Python e importa las funciones principales.

**Funcionalidad:**
- Importa `adelante`, `abajo` y `reiniciar` desde `draewer_logic.py`
- Define `__version__` = "1.0.0" para versionado
- Define `__all__` para controlar qué se exporta al hacer `from mini_turtle import *`

**Uso:**
```python
from mini_turtle import adelante, abajo, reiniciar
```

## Reto 2

### 2. `mini_turtle/draewer_logic.py`
**Qué es:** Módulo que contiene la lógica de dibujo ASCII.

**Variables globales:**
- `posicion_x`: posición horizontal del cursor (0 por defecto)
- `posicion_y`: posición vertical del cursor (0 por defecto)

**Funciones:**

#### `adelante(pasos)`
- **Qué hace:** dibuja una línea horizontal usando guiones (`-`) y termina con `>`
- **Parámetros:** `pasos` (int) — número de caracteres `-` a dibujar
- **Efecto:** incrementa `posicion_x` en la cantidad de pasos
- **Ejemplo:**
  ```
  adelante(7)  # Output: --------->
  ```

#### `abajo(pasos)`
- **Qué hace:** dibuja una línea vertical usando `|` y termina con `V`
- **Parámetros:** `pasos` (int) — número de líneas con `|` a dibujar
- **Efecto:** incrementa `posicion_y` en la cantidad de pasos
- **Ejemplo:**
  ```
  abajo(3)  # Output:
            # |
            # |
            # V
  ```

#### `reiniciar()`
- **Qué hace:** reinicia las posiciones a (0, 0)
- **Parámetros:** ninguno
- **Efecto:** resetea `posicion_x` y `posicion_y` a 0
- **Uso:** limpia el estado antes de un nuevo dibujo

### 3. `main.py`
**Qué es:** Script de ejemplo que demuestra el uso de las funciones.

**Flujo:**
1. Reinicia posición
2. Dibuja línea de 7 caracteres hacia adelante
3. Dibuja línea de 3 caracteres hacia abajo
4. Reinicia de nuevo
5. Dibuja línea de 5 adelante y 5 abajo
6. Dibuja línea de 3 adelante y 7 abajo

**Cómo ejecutar:**
```bash
python main.py
```



**Incluye:**
- `__pycache__/` — caché compilado de Python
- `*.py[cod]` — archivos compilados
- `.venv/` — entorno virtual
- Directorios de cobertura, tests y build
- Archivos de IDE y configuración local

## Cómo usar el proyecto

### 1. Clonar y entrar al directorio
```bash
git clone <repo> && cd project_mini_turtle
```

### 3. Ejecutar el programa
```bash
python main.py
```

### 4. (Opcional) Importar en otros scripts
```python
from mini_turtle import adelante, abajo, reiniciar

reiniciar()
adelante(10)
abajo(5)
```

## Licencia
Este proyecto está bajo licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## Notas prácticas
- Las funciones usan `print()` para mostrar caracteres en la terminal
- Las posiciones se rastrean con variables globales
- El sistema de coordenadas es simple: solo se rastrea X (horizontal) e Y (vertical)
- Para ver cambios en la lógica, edita [mini_turtle/draewer_logic.py](mini_turtle/draewer_logic.py)


### Referencias ⚠️

- Conversaciones con claude
- Tutoriales de Youtube

*Última actualización: 11/12/2025*
