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













