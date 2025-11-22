## Implementando una tortuga desde cero 🐢


## Reto 1

- En base al código suministrado por el profesor se agrega la función **print**, ya que en la entrada buscamos que brinde un saludo o contexto y se usa la función **input** para indicar al usuario cuantos pasos desea que recorra la turtuga.

**Código usado en el reto1**

```python
**import turtle

print("Creando una tortuga simulada ... que da pasos")
input("Cuantos pasos deseas que de la tortuga...")
t = turtle.Turtle()
t.shape("turtle")
t.speed(1) # 1:slowest, 3:slow, 5:normal, 10:fastest
t.color("Green")
t.forward(100)
turtle.done()         # Mantiene la ventana abierta
print("La tortuga ha terminado de caminar.")
print("Programa terminado.")**

```

![](https://github.com/g23-png/g23-png.io/blob/main/Reto%201.png)

**Se realiza estudio por medio de videos en internet en el cual se le brindo una forma a la tortuga, se asigna una velocidad y un color.**


## Reto 2

- Segun la información documentada debemos realizar que una vez la tortuga camine los pasos realize un giro de 90 grados

**Código usado en el reto2**

```python

import turtle

print("Creando una tortuga simulada ... que da pasos")
input("Cuantos pasos deseas que de la tortuga...")
t = turtle.Turtle()
t.shape("turtle")
t.speed(1) # 1:slowest, 3:slow, 5:normal, 10:fastest
t.color("Green")
t.forward(100)
t.right(90)
turtle.done()         # Mantiene la ventana abierta
print("La tortuga ha terminado de caminar.")
print("Programa terminado.")

```
![](https://github.com/g23-png/g23-png.io/blob/main/Reto%202.png)



## Reto 3

- La tortuga ya dio sus primeros pasos, aprendio a girar y con ello llevo los pasos a otro nivel, es algo que podemos ver en el código agregando un **t.forward** con la cantidad de pasos deseada

** Código usado en el reto3**

```python

import turtle

print("Creando una tortuga simulada ... que da pasos")
input("Cuantos pasos deseas que de la tortuga...")
t = turtle.Turtle()
t.shape("turtle")
t.speed(1) # 1:slowest, 3:slow, 5:normal, 10:fastest
t.color("Green")
t.forward(100)
t.right(90)
t.forward(100)
turtle.done()         # Mantiene la ventana abierta
print("La tortuga ha terminado de caminar.")
print("Programa terminado.")

```
![](https://github.com/g23-png/g23-png.io/blob/main/Reto%203.png)


## Reto 4

- Se busca que la tortuga siga caminando y creando la L, pero creando unas nuevas funciones. En este reto aprendi adicional a generar cambios en el color del fondo y tener una linea más gruesa

** Código usado en el reto4**

```python

import turtle

# Definir las funciones para encapsular los movimientos
def adelante(n):
    """Dibuja el movimiento hacia la derecha (→) por n pasos"""
    t.forward(n)

def abajo(n):
    """Dibuja el movimiento hacia abajo (↓) por n pasos"""
    t.right(90)
    t.forward(n)

print("Creando una tortuga simulada ... que da pasos")
input("Cuantos pasos deseas que de la tortuga...")

# Crear la tortuga
t = turtle.Turtle()
t.shape("turtle")
turtle.bgcolor("#BAF08B")
t.speed(1)  # 1:slowest, 3:slow, 5:normal, 10:fastest
t.color("Green")
t.pencolor("black")
t.pensize(3)

# Usar las funciones para crear el patrón en forma de L
adelante(50)
abajo(30)

turtle.done()  # Mantiene la ventana abierta
print("La tortuga ha terminado de caminar.")
print("Programa terminado.")

```

![](https://github.com/g23-png/g23-png.io/blob/main/Reto%204.png)


## Reto 5

- Ahora el reto es mayor, ya que la tortuga debe bajar escalas, se realiza un cambio en el código, ya que cada vez que llamaba abajo la tortuga giraba 90 grados y estaba realizando un circulo, con ayuda de una inteligencia artificial descubri el error.

** Código usado en el reto5**

```python

import turtle

# Definir las funciones para encapsular los movimientos
def adelante(n):
    """Dibuja el movimiento hacia la derecha (→) por n pasos"""
    t.setheading(0)  # Asegura que mire hacia la derecha (0°)
    t.forward(n * 10)  # Multiplicamos por 10 para hacer pasos más visibles

def abajo(n):
    """Dibuja el movimiento hacia abajo (↓) por n pasos"""
    t.setheading(270)  # Asegura que mire hacia abajo (270°)
    t.forward(n * 10)  # Multiplicamos por 10 para hacer pasos más visibles

print("Creando una tortuga simulada ... que da pasos")
input("Presiona Enter para comenzar...")

# Crear la tortuga
t = turtle.Turtle()
t.shape("turtle")
turtle.bgcolor("#BAF08B")
t.speed(2)  # Un poco más rápido para ver mejor el patrón
t.color("Green")
t.pencolor("black")
t.pensize(3)

# Dibujar los escalones según el ejemplo
# Escalón 1
adelante(5)
abajo(2)

# Escalón 2
adelante(5)
abajo(2)

# Escalón 3
adelante(3)
abajo(2)

turtle.done()  # Mantiene la ventana abierta
print("La tortuga ha terminado de caminar.")
print("Programa terminado.")

```

![](https://github.com/g23-png/g23-png.io/blob/main/Reto%205.png)


### Referencias ⚠️

- Conversaciones con claude
- Tutoriales de Youtube

*Última actualización: 21/11/2025*
