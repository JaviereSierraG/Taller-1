# Taller 1 Programación Pythorque
En este repositorio se documenta el desarrollo del primer taller realizado por Javier Sierra.

## 1.Desarrollo Quiz Python

![Texto alternativo](https://github.com/JaviereSierraG/Taller-1/blob/main/SCquiz.png)

## 2. Realice un programa que lea tres números reales y determine cuál es el mayor.
```python
numero1 = float(input("Ingrese el primer número: "))
numero2 = float(input("Ingrese el segundo número: "))
numero3 = float(input("Ingrese el tercer número: "))

# Determina cuál es el mayor
if numero1 >= numero2 and numero1 >= numero3:
    mayor = numero1
elif numero2 >= numero1 and numero2 >= numero3:
    mayor = numero2
else:
    mayor = numero3

# Imprime el resultado
print("El número mayor es:", mayor)
```


Primero damos la entrada para los tres números como flotante y luego usamos las estructuras de control para describir las posibles relaciones y las salidas del código. 

## 3. Realice un programa que lea un número enteros y determine si es par o impar. 

```python
#Notebook
numero = float(input("Ingrese el número:"))

if numero % 2 == 0:
    print(numero, "es un número par")

else:
   print(numero, "es un número impar")
```
Primero creamos la entrada de tipo flotante para ingresar el número y luego usamos el módulo para conocer el residuo de la división del número entre 2 y asi determinar si es par o inpar.

## 4. Realice un programa que lea dos números reales y determine si el primero es múltiplo.
```python
numero1 = float(input("Ingrese el primer número:"))
numero2 = float(input("Ingrese el segundo número:"))

if numero1 % numero2 == 0:
  print(numero1, "es múltiplo del segundo número")

else:
  print(numero1,"no es múltiplo del segundo número")****
```
Creamos la entrada de tipo flotante para los dos número especificando su orden, nos volvemos a valer del módulo para conocer si la división del primer número entre el segundo deja algún residuo y así determinar si es múltiplo o no.

## 5. Realice un programa que lea tres números reales y determine si la suma de los dos primeros es mayor, menor o igual que el tercer número.
```python
#Notebook
numero1 = float(input("Ingrese el primer número: "))
numero2 = float(input("Ingrese el segundo número: "))
numero3 = float(input("Ingrese el tercer número: "))

if numero1 + numero2 > numero3:
  print(numero1, "+", numero2,"=", numero1 + numero2,  ">", numero3)
elif numero1 + numero2 == numero3:
  print(numero1, "+", numero2,"=", numero1 + numero2,  "=", numero3)
else:
  print( numero1, "+" ,numero2, "=", numero1 + numero2, "<", numero3)
```
Empezamos creando las entradas de tipo flotante para los 3 números, luego utilizamos las estructuras del control con condiciones especificas para en cada caso arrojar la salida correcta, tuvimos en cuenta también una posible igualdad aunque no se mencionara en el ejercicio. Asi teniendo 3 posibles resultado mayor que, menor que e igual.

## 6. Escriba un programa que solicite al usuario una letra y determine si es una vocal o una consonante.

```python
letra = str(input("Ingrese una letra: "))

letra = letra.lower()

if letra in ('a', 'e', 'i', 'o', 'u'):
    print(letra, " es una vocal.")
else:
    print(letra, "es una consonante.")
```
Para este ejercicio utilizamos una entrada de tipo cadena para garantizar la naturalidad de la respuesta, asi mismo utilizamos las vocales para descartar el resto de letras, asi pues asegurandonos que la entrada no sea ninguna de las 5 vocales, garantizamos que sea una consonante, o en su caso contrario confirmamos que es una vocal. Utilice letra.lower( ) para simplificar el código.

## 7. Escriba un programa que pida 5 números reales y calcule las siguientes operaciones: El promedio,la mediana, promedio multiplicativo, calcule la potencia del mayor número al menor número y calcule la raíz del menor número.
```python
# Solicita al usuario ingresar 5 números reales
numeros = []
for i in range(5):
    numero = float(input(f"Ingrese el número {i+1}: "))
    numeros.append(numero)

# Calcula el promedio
promedio = sum(numeros) / len(numeros)

# Calcula la mediana
numeros_ordenados = sorted(numeros)
if len(numeros_ordenados) % 2 == 0:
    mediana = (numeros_ordenados[len(numeros_ordenados)//2 - 1] + numeros_ordenados[len(numeros_ordenados)//2]) / 2
else:
    mediana = numeros_ordenados[len(numeros_ordenados)//2]

# Calcula el promedio multiplicativo
producto = 1
for numero in numeros:
    producto *= numero
promedio_multiplicativo = producto ** (1/len(numeros))

# Ordena los números de forma ascendente y descendente
numeros_ascendente = sorted(numeros)
numeros_descendente = sorted(numeros, reverse=True)

# Calcula la potencia del mayor número elevada al menor número
mayor_numero = max(numeros)
menor_numero = min(numeros)
potencia = mayor_numero ** menor_numero

# Calcula la raíz cúbica del menor número
raiz_cubica = menor_numero ** (1/3)

# Imprime los resultados
print("Promedio:", promedio)
print("Mediana:", mediana)
print("Promedio multiplicativo:", promedio_multiplicativo)
print("Números en orden ascendente:", numeros_ascendente)
print("Números en orden descendente:", numeros_descendente)
print("Potencia del mayor número elevada al menor número:", potencia)
print("Raíz cúbica del menor número:", raiz_cubica)
```
Primero, se solicita al usuario ingresar los 5 números. Esto se logra mediante un bucle for que se ejecuta 5 veces, cada vez solicitando al usuario que ingrese un número real. Los números ingresados se almacenan en una lista llamada numeros.

Luego de obtener los números, se procede a realizar los siguientes cálculos:

Promedio:
Se calcula sumando todos los números en la lista y dividiendo la suma por la cantidad de números en la lista. Esto nos da el promedio de los números ingresados.

Mediana:
Los números se ordenan de forma ascendente y luego se determina si la cantidad de números es par o impar. Si es par, la mediana se calcula como el promedio de los dos números centrales. Si es impar, la mediana es simplemente el número central.

Promedio Multiplicativo:
Se multiplican todos los números en la lista y luego se calcula la raíz enésima del producto, donde n es la cantidad de números en la lista. Esto nos da el promedio multiplicativo de los números.

Ordenar los números:
Los números se ordenan de forma ascendente y descendente utilizando la función sorted(). Se obtienen dos listas: una en orden ascendente y otra en orden descendente.

Potencia del Mayor Número:
Se determina el mayor y el menor número en la lista. Luego se eleva el mayor número a la potencia del menor número.

Raíz Cúbica del Menor Número:
Se calcula la raíz cúbica del menor número en la lista.

Finalmente, se imprimen los resultados de todos estos cálculos.










