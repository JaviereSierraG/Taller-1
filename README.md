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


Primero damos la entrada para los tres números como flotante y luego usamos las estructuras de control para describir las posibles relaciones y las salidas del código. 
