# Mi Primera Página Web - Aprendizaje de Programación 🎯 

## Bienvenido a mi sitio

¡Hola! 

Soy Daniel Gonzalez y esta es mi primera página web creada con GitHub Pages. Aquí documentaré mi aprendizaje en programación visto en las clases con el profesor Juan Camilo Masias.

---

## Temas Vistos en Clase 📚

### ¿Qué es un programa?
Un programa es un conjunto de instrucciones que le decimos a la computadora para que realice una tarea específica. Los programas se escriben en lenguajes de programación como Python, JavaScript, Java, etc.

### ¿Qué es un algortimo?
Un algoritmo es una secuencia finita y ordenada de pasos o instrucciones que se siguen para resolver un problema o realizar una tarea específica. Es como una receta de cocina: tienes ingredientes (datos de entrada) y sigues pasos específicos para obtener un resultado (salida).

**Caracteristicas de un algoritmo**
**Finito:** Debe terminar después de un número determinado de pasos

**Definido:** Cada paso debe estar claramente especificado

**Entrada:** Puede tener cero o más datos de entrada

**Salida:** Debe producir al menos un resultado

**Efectivo:** Cada operación debe ser básica y realizable

### Variables en Python
Las variables son contenedores donde guardamos información que podemos usar y modificar más adelante. En Python, crear una variable es muy simple, siempre y cuando se respeten los pasos que se tiene establecidos o como base:

**Ejemplo de código:**
```python
# Declaración de variables
nombre = "María"
edad = 20
altura = 1.65
es_estudiante = True

# Usando las variables
print(f"Hola, me llamo {nombre}")
print(f"Tengo {edad} años y mido {altura} metros")

# Operaciones con variables
edad_futura = edad + 5
print(f"En 5 años tendré {edad_futura} años")
```

### Tipos de Datos
Python maneja diferentes tipos de datos:
- **String (str)**: texto, como `"Hola mundo"`
- **Integer (int)**: números enteros, como `42`
- **Float**: números decimales, como `3.14`
- **Boolean (bool)**: valores verdadero/falso, como `True` o `False`

---

## Ejemplo Práctico: Calculadora Simple
```python
# Programa simple de calculadora
numero1 = float(input("Ingresa el primer número: "))
numero2 = float(input("Ingresa el segundo número: "))

suma = numero1 + numero2
resta = numero1 - numero2
multiplicacion = numero1 * numero2
division = numero1 / numero2

print(f"Suma: {suma}")
print(f"Resta: {resta}")
print(f"Multiplicación: {multiplicacion}")
print(f"División: {division}")
```

---

## Reflexión Personal 💡

Al comenzar con la programación, me di cuenta de que es como aprender un nuevo idioma. La sintaxis de Python me parece compleja, especialmente con las indentaciones (espacios al inicio de cada línea). Sin embargo, después de practicar con varios ejemplos, empecé a entender la lógica detrás del código, teniendo en cuenta que cada vez que practico pongo en función lo aprendido y con los errores que he comedito he aprendido de ellos.

De las cosas que más me han sorprendió son las variables. Con algo tan simple puedo guardar información y reutilizarla cuantas veces quiera. Es interesante ver el progreso que he presentado a la fecha.


**Mis objetivos:**
- Practicar diariamente con ejercicios de Python, ver videos tutoriales en youtube para fortalecer los conocimientos.
- Crear pequeños proyectos para aplicar lo aprendido.
- Documentar todo mi progreso en esta página.
- Practicar en foros, en los cuales puedo exponer novedades que he presentado o resolver dudas de otras personas.

---

## Recursos Útiles

- [Documentación oficial de Python](https://docs.python.org/es/)
- [Tutorial de GitHub Pages](https://docs.github.com/es/pages)

---

### Referencias ⚠️

- Conversaciones con chat GPT
- Conversaciones con Claude
- GitHub Learning Lab

  ---


## Implementando una tortuga desde cero


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


*Última actualización: 21/11/2025*
