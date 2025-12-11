## El reto de una tortuga desde cero 🐢

## Que se busca

Implemetar funciones basicas de Python, en las cuales vamos a realizar una similación de nuestra tortuga. Se va a documentar la información sobre este proyecto y se explica la funcionalidad del mismo.


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



## Reto 3

**Ahora la tortuga no solo avanza: también gira.**

- Para dar una solución a que la tortuga se pueda desplazar hacia abajo, procedo a dejar unos espacios en el código.

- **Nota:** Tener en cuenta que si excede de 5 a más pasos el desplazamiento puede fallar

** Código usado en el reto3**

```python

def reto_uno(pasos):
    print("Nuestra  tortuga ahora avanza adelante y tambien baja")
    print("-" * pasos + ">")

def reto_dos(abajo_pasos):
    for i in range(abajo_pasos):
        print("    |")
    print("    V")
reto_uno(5)
reto_dos(3)

```


## Reto 4

**Reescribe los retos anteriores creando funciones que representen los movimientos de la tortuga solo con texto.**

- En esta ocasión el usuario puede indicar cuantos pasos avanza y adicional cuantos pasos puede bajar la tortuga

** Código usado en el reto4**

```python

pasos_adelante = int(input("¿Cuántos pasos avanza la tortuga? "))
pasos_abajo = int(input("¿Cuántos pasos baja la tortuga? "))

def adelante(pasos):
    if pasos >= 50:
        print("No se permiten más de 50 pasos hacia adelante.")
    else:
        # Dibuja la flecha hacia adelante
        print("-" * pasos + ">")

def abajo(pasos, espacio_izquierdo):
    # Dibuja la bajada alineada con el final de la flecha
    for i in range(pasos):
        print(" " * espacio_izquierdo + "|")
    
    print(" " * espacio_izquierdo + "V")

adelante(pasos_adelante)
abajo(pasos_abajo, pasos_adelante)

pasos_totales = pasos_adelante + pasos_abajo
print("La tortuga recorrió un total de", pasos_totales, "pasos.")
print("¡Felicidades la tortuga culmino su reccorido!")

```


## Reto 5

**Ajusta tus funciones para que la tortuga pueda bajar escalones.
Cada escalón debe conservar la posición horizontal acumulada y dibujar correctamente tanto el tramo horizontal como el vertical.**

- Ahora el reto es mayor, ya que la tortuga debe bajar escalas, se realiza un cambio en el código, ya que cada vez que llamaba abajo la tortuga giraba 90 grados y estaba realizando un circulo, con ayuda de una inteligencia artificial descubri el error.

** Código usado en el reto5**

```python

pasos_adelante = int(input("¿Cuántos pasos avanza la tortuga? "))
pasos_abajo = int(input("¿Cuántos pasos baja la tortuga? "))

# Creamos una variable para saber cuántos escalones dibujar
cantidad_escalones = int(input("¿Cuántos escalones bajará la tortuga? "))

# Estas variables nos ayudan a llevar la cuenta de los espacios y pasos
espacios_acumulados = 0 
pasos_totales = 0

def adelante(pasos, espacios_al_inicio):
    # Hacemos una verificación para que no se pase de 50 pasos
    if pasos >= 50:
        print("No se permiten más de 50 pasos hacia adelante.")
        return
    else:
        # imprimimos los espacios y luego los guiones con la flecha
        espacios = " " * espacios_al_inicio
        flecha = "-" * pasos + ">"
        print(espacios + flecha)

def abajo(pasos, espacios_al_inicio):
    # Dibujamos los pasos de bajada
    for i in range(pasos):
        print(" " * espacios_al_inicio + "|")
    
    # Colocamos la flecha hacia abajo al final
    print(" " * espacios_al_inicio + "V")

# Repetimos el proceso para cada escalón
for i in range(cantidad_escalones):
    
    # 1. Avanzamos hacia adelante
    adelante(pasos_adelante, espacios_acumulados)
    
    # 2. Acumulamos los espacios para el próximo escalón
    espacios_acumulados = espacios_acumulados + pasos_adelante
    
    # 3. Bajamos hacia abajo
    abajo(pasos_abajo, espacios_acumulados)
    
    # Se suman los pasos al total
    pasos_totales += pasos_adelante + pasos_abajo

print("La tortuga recorrió un total de", pasos_totales, "pasos.")

```


### Referencias ⚠️

- Conversaciones con claude
- Tutoriales de Youtube

*Última actualización: 9/12/2025*
