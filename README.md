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
Este código en Python comienza solicitando al usuario ingresar 5 números reales. Para hacer esto, se utiliza un bucle for para iterar 5 veces, solicitando al usuario que ingrese cada número. Dentro del bucle, se utiliza la función input() para capturar la entrada del usuario, y luego se convierte a tipo float para garantizar que los números ingresados sean reales. Los números ingresados se agregan a una lista llamada numeros.

Después de obtener los números, el código procede a realizar varios cálculos:

Promedio:
Para calcular el promedio de los números ingresados, se utiliza la función sum() para sumar todos los números en la lista numeros, y luego se divide la suma por la cantidad de números en la lista (len(numeros)).

Mediana:
Para calcular la mediana, los números en la lista numeros se ordenan de forma ascendente utilizando la función sorted(). Luego, se verifica si la cantidad de números es par o impar, y se calcula la mediana en consecuencia.


Promedio Multiplicativo:
Para calcular el promedio multiplicativo, se inicializa una variable producto en 1 y se utiliza un bucle for para multiplicar todos los números en la lista numeros. Luego, se calcula el promedio multiplicativo elevando el producto a la potencia de 1 dividido por la cantidad de números en la lista.

Ordenar los números:
Para ordenar los números de forma ascendente y descendente, se utilizan las funciones sorted() con y sin el argumento reverse=True, respectivamente.

Potencia del Mayor Número:
Para calcular la potencia del mayor número elevada al menor número, se utilizan las funciones max() y min() para obtener el mayor y el menor número en la lista numeros. Luego, se eleva el mayor número a la potencia del menor número.

Raíz Cúbica del Menor Número:
Para calcular la raíz cúbica del menor número en la lista, se utiliza la operación de potenciación **(1/3).

Finalmente, se imprimen los resultados de todos estos cálculos.

Este código proporciona una comprensión más clara de cómo se realizan los cálculos y qué partes del código se utilizan para cada paso específico.

## 8.Escriba un programa al que se le ingrese la frecuencia de una onda en hz y como salida arroje en que parte del espectro electromagnético se encuentra.
```python
# Solicita al usuario ingresar la frecuencia en Hz
frecuencia = float(input("Ingrese la frecuencia en Hz: "))

# Determina en qué parte del espectro electromagnético se encuentra la frecuencia
if 3e23 < frecuencia < 3e25:
    print("La frecuencia está en la parte de los rayos gamma.")
elif 3e19 < frecuencia <= 3e23:
    print("La frecuencia está en la parte de los rayos X.")
elif 4.3e14 < frecuencia <= 3e19:
    print("La frecuencia está en la parte de los rayos ultravioleta.")
elif 7.5e11 < frecuencia <= 4.3e14:
    print("La frecuencia está en la parte del espectro visible.")
elif 3e9 < frecuencia <= 7.5e11:
    print("La frecuencia está en la parte de las ondas de radio.")
else:
    print("La frecuencia está fuera del espectro electromagnético conocido.")

```
Creamos la entrada como flotante especificando que debe ser una frecuencia en hertz, luego utilizando las sentencias de control creamos rangos entre los que puede variar esa frecuencia y así creando fronteras entre los distintos espectros de frecuencia podemos clasificarlas y conocer la parte del espectro en la que se encuentran. 

## 9. Escriba un programa que reciba el nombre en minúsculas de un país de América y regrese la ciudad capital, si el país no pertenece al continente debe arrojar país no identificado.
```python
#Notebook
# Diccionario de capitales de países de América
capitales_americas = {
    "argentina": "Buenos Aires",
    "bolivia": "La Paz",
    "brasil": "Brasilia",
    "canada": "Ottawa",
    "chile": "Santiago",
    "colombia": "Bogotá",
    "costa rica": "San José",
    "cuba": "La Habana",
    "ecuador": "Quito",
    "el salvador": "San Salvador",
    "estados unidos": "Washington D.C.",
    "guatemala": "Ciudad de Guatemala",
    "honduras": "Tegucigalpa",
    "mexico": "Ciudad de México",
    "nicaragua": "Managua",
    "panama": "Panamá",
    "paraguay": "Asunción",
    "peru": "Lima",
    "uruguay": "Montevideo",
    "venezuela": "Caracas",
    "dominica": "Roseau",
    "ecuador": "Quito",
    "granada": "Saint George's",
    "haiti": "Puerto Príncipe",
    "jamaica": "Kingston",
    "saint kitts and nevis": "Basseterre",
    "saint lucia": "Castries",
    "saint vincent and the grenadines": "Kingstown",
    "suriname": "Paramaribo",
    "trinidad and tobago": "Puerto España"
}

# Solicita al usuario ingresar el nombre de un país en minúsculas
pais = input("Ingrese el nombre del país en minúsculas: ")

# Busca la capital del país en el diccionario
capital = capitales_americas.get(pais, "país no identificado")

# Imprime la capital del país o un mensaje si no se encontró el país en el diccionario
print("La capital de", pais.capitalize(), "es:", capital)

```
Desconociendo si existe una herramienta en linea que busque las capitales de los países, decidi realizar una lista con todos los países de latinoámerica y sus clases para luego en la entrada solicitar el nombre del país en miniscula y así se ejecute la lista para entregar la respuesta. 

## 10. Escriba un programa que dada una distancia calcula:

El tiempo que le tomaría a la luz recorrer la distancia.

El tiempo que le tomaría al sonido (en el aire) recorrer la distancia.

El tiempo que le tomaría al vehículo comercial más veloz recorrer la distancia.

El tiempo que le tomaría a Bolt recorrer la distancia.







