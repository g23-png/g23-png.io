## Implementando una tortuga desde cero 🐢


## Reto 1

**Simula el comportamiento de la tortuga usando solo print() e input().**

**Intenta recrear el movimiento de la tortuga únicamente con texto, usando funciones, print() y input() para pedir valores al usuario.**

- Se agrega la función print para imprimir el enunciado sobre la tortuga, se agregan los caracteres de guiones y signos para marcar los pasos y final de los mismos

**Código usado en el reto1**

```python
def reto_uno(pasos):
    print("Creando tortuga simulada que da... 50 pasos")
    print("-" * pasos + ">")
    return

reto_uno(50)

```

![](https://github.com/g23-png/g23-png.io/blob/main/Reto%201.png)

**Se realiza estudio por medio de videos en internet en el cual se le brindo una forma a la tortuga, se asigna una velocidad y un color.**


## Reto 2

**Tortuga bajando**

**Crea el rastro de una tortuga moviéndose hacia abajo usando únicamente print() e input().**

- Con la función **print** se indica la cantidad la cantidad de pasos que va a dar la tortuga  la dirección, se usa **for i in range(pasos):** para repetir la secuencia **N** veces que se agregue en el código.

**Código usado en el reto2**

```python

def reto_dos(pasos):
    # Dibujamos los pasos de bajada
    print("Dibujando la bajada de la tortuga, la cual va a dar 5 pasos:")
    for i in range(pasos):
        print("|")
    
    # Colocamos la flecha hacia abajo al final
    print("V")

reto_dos(5)

```
![](https://github.com/g23-png/g23-png.io/blob/main/Reto%202.png)



## Reto 3

**Ahora la tortuga no solo avanza: también gira.**

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

**Reescribe los retos anteriores creando funciones que representen los movimientos de la tortuga solo con texto.**

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

**Ajusta tus funciones para que la tortuga pueda bajar escalones.
Cada escalón debe conservar la posición horizontal acumulada y dibujar correctamente tanto el tramo horizontal como el vertical.**

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
