# reto-9

##1. De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.
```pseoducode
if __name__ == "__main__":
    # Se solicita al usuario ingresar la cantidad de gallinas, gallos y pollitos.
    N = float(input("Ingrese la cantidad de gallinas: "))
    M = float(input("Ingrese la cantidad de gallos: "))
    k = float(input("Ingrese la cantidad de pollitos: "))
    # Se define una lambda para calcular la cantidad de carne de aves.
    cantidadDeCarneAves = lambda N, M, k: (N * 6) + (M * 7) + k
    # Se llama a la lambda con los valores ingresados por el usuario.
    cantidadDeCarne = cantidadDeCarneAves(N, M, k)
    # Se muestra el resultado.
    print("La cantidad de carne de aves es de: " + str(cantidadDeCarne) + " kg")
```
```pseoducode
if __name__ == "__main__":
    # Se solicita al usuario ingresar el valor del billete y las cantidades de panes, huevos y leche.
    pesos = float(input("Ingrese el valor del billete: "))
    pan = float(input("Ingrese la cantidad de panes: "))
    huevos = float(input("Ingrese la cantidad de huevos: "))
    leche = float(input("Ingrese la cantidad de leche: "))
    # Se define una lambda para calcular el costo de la compra.
    costo = lambda pan, huevos, leche: (pan * 300) + (leche * 3300) + (huevos * 350)
    # Se calcula el costo de la compra utilizando la lambda y las cantidades ingresadas.
    valor = costo(pan, huevos, leche)
    # Se calcula el cambio o la cantidad faltante.
    p = pesos - valor
    # Se comprueba si el monto ingresado es suficiente y se muestra el resultado correspondiente.
    if pesos > valor:
        print("Sus vueltas son " + str(p) + " pesos")
    if valor > pesos:
        print("Usted debe " + str(-p) + " pesos")

```
```pseoducode
if __name__ == "__main__":
    # Se solicita al usuario ingresar el número actual de contagiados y el número de días a partir de hoy.
    C = float(input("Ingrese el número actual de contagiados: "))
    D = float(input("Ingrese el número de días a partir de hoy: "))
    # Se define una lambda para calcular el número total de contagiados.
    totalContagiados = lambda C, D: C * (2 ** D)
    # Se llama a la lambda con los valores ingresados por el usuario.
    contagiados = totalContagiados(C, D)
    # Se muestra el resultado.
    print("El número total de personas contagiadas después de " + str(D) + " días es: " + str(contagiados))
```
##2. De los retos anteriores seleciones 3 funciones y escribalas con argumentos no definidos (*args).
```pseoducode
def totalContagiados(*args):
    # extraer los argumentos en las variables C y D
    C, D = args
    return C * (2 ** D)
# Se solicita al usuario ingresar el número actual de contagiados y el número de días a partir de hoy.
C = float(input("Ingrese el número actual de contagiados: "))
D = float(input("Ingrese el número de días a partir de hoy: "))
# Llamar a la función totalContagiados con los valores ingresados por el usuario
contagiados = totalContagiados(C, D)
# Mostrar el resultado
print("El número total de personas contagiadas después de " + str(D) + " días es: " + str(contagiados))

```
```pseoducode
import math

def perimetroAreaFigura(*args):
    # extraer los argumentos en las variables radio, base y altura
    radio, base, altura = args
    # Cálculo del perímetro
    perimetro = (2 * (2 * radio * math.pi)) + (2 * (base * altura))
    # Cálculo del área
    area = (math.pi * (radio ** 2)) + (base * altura)
    # Devolver los resultados como una tupla (perimetro, area)
    return perimetro, area
if __name__ == "__main__":
    # Solicitar al usuario ingresar el radio del círculo, la base y la altura del rectángulo
    radio = float(input("Ingrese el radio del círculo: "))
    base = float(input("Ingrese la base del rectángulo: "))
    altura = float(input("Ingrese la altura del rectángulo: "))
    # Llamar a la función perimetroAreaFigura con los valores ingresados por el usuario
    perimetro, area = perimetroAreaFigura(radio, base, altura)
    # Mostrar el área y el perímetro de la figura
    print("El área de la figura es: " + str(area))
    print("El perímetro de la figura es: " + str(perimetro))

```
```pseoducode
def calculoPrestamo(*args):
    # extraer los argumentos en las variables C, i y n
    C, i, n = args
    # Calcular el valor final del préstamo utilizando la fórmula
    valor = C * (1 + ((i / 100) / 12)) ** n

    # Devolver el valor final del préstamo
    return valor
if __name__ == "__main__":
    # Solicitar al usuario ingresar el valor del préstamo inicial, la tasa de interés y el número de meses
    C = float(input("Ingrese el valor del préstamo inicial: "))
    i = float(input("Ingrese la tasa de interés: "))
    n = float(input("Ingrese el número de meses: "))
    # Llamar a la función calculoPrestamo con los valores ingresados por el usuario
    valorFinal = calculoPrestamo(C, i, n)
    # Mostrar el valor final del préstamo
    print("El valor del préstamo después de " + str(n) + " meses es de: " + str(valorFinal))
```
3.Escriba una función recursiva para calcular la operación de la potencia.
 ```pseoducode
 def potencia(base:int, exponente:int)->int:
    # Caso base: si el exponente es 0, el resultado es 1
    if exponente == 0:
        return 1  
    # Caso recursivo: calcula la potencia utilizando la recursión
    return base * potencia(base, exponente)
if __name__ == "__main__":
 #pide la base al usuario
 base=(input("ingrese la base ")) 
 #pide el exponente al usuario
 exponente=(input("ingrese el exponente "))
 #llama la función
 calculo = potencia(base, exponente)
 #imprime el resultado
 print(calculo)
 ```
 4. Utilice la siguiente plantilla de code para contar el tiempo:
  ```pseoducode
  import time
# Función para calcular la serie de Fibonacci de forma iterativa
def fibonacciInter(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        a, b = 0, 1
        for i in range(2, n + 1):
            a, b = b, a + b
        return b
# Función para calcular la serie de Fibonacci de forma recursiva
def fibonacciRecur(n):
    if n <= 0:
        return 0
    elif n == 1:
        return 1
    else:
        return fibonacciRecur(n - 1) + fibonacciRecur(n - 2)
# Medición del tiempo de ejecución para la función iterativa
TI = time.time()  # Tiempo de inicio
n = 35
fibonacciInter(n)  # Llamada a la función iterativa
TF = time.time()  # Tiempo de finalización
t = TF - TI  # Cálculo del tiempo transcurrido
print("Tiempo de ejecución iterativo para n: " + str(n) + ": " + str(t) + " segundos")
# Medición del tiempo de ejecución para la función recursiva
TI = time.time()  # Tiempo de inicio
n = 30
fibonacciRecur(n)  # Llamada a la función recursiva
TF = time.time()  # Tiempo de finalización
t = TF - TI  # Cálculo del tiempo transcurrido
print("Tiempo de ejecución recursiva para n: " + str(n) + ": " + str(t) + " segundos")

   ```
  #enlace stackoverflow https://stackoverflow.com/users/21890977/santiago-nicolas-linares-gonza 
  #enlace linkedin https://www.linkedin.com/in/santiago-linares-39280b276/
