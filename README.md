# Funciones_peroparte_2-Reto-9
Realizaremos los ejercicios impuestos en clase que ayudaras a entender como usar lambdas, funciones sin argumento etc.
## Punto 1:
- De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.
### Eplicación: ###
Tome la misma metodología para las tres, se supone que las lambdas son para operaciones sencillas y es una forma de simplificar todo en una sola linea, como ve puse las funciones en las que se baso en comentarios.

```
#def valor_total_prestamo( C: float,i: float,n:int):
   #  valor = C * ((1 + i)**n)
   #  return valor

Valor_prestamos=lambda C,i,n: C * ((1 + i)**n)
# ESta funcion lambda halla el valor de un prestamo
#Argurmentos:
# C(float): cantidad del prestamo
# i(float): valor del interes
# n(int): cantidad de meses
# el resulyado devolvera el valor del prestamo
print(Valor_prestamos(2,23,2))
```
```
#def calcula_cant_carne_en_Aves ( N:int, M:int ,K:int) : #se declaran

# total_de_carne = (N*6)+(M*7)+(K*1) # operacion principal (6 de gallinas, 7 de gallos, 1 de pollitos) #peso en kg
# Cant_kilos= total_de_carne/1000
# return Cant_kilos#lo que debe arrojar la funcion

Cantidad_de_carnes=lambda N,M,K: ((N*6)+(M*7)+(K*1))/1000
#Esta funcion halla la cantidad de kilos que hay entre tres animales segun su peso
#Argumentos:
# N(int): cantidad de gallinas
# M(int): cantidad de gallos
# K(int): cantidad de pollitos
# Devolvera el total de kilos que hay en total segun la cantidad de animales que hayan
print(Cantidad_de_carnes(3,5,7))

```
```
#def contagiados_porDias(C:int,D:int):
#    total_contagiadoscovid = C * (2**D) #operacion para hallar contagiados a partir de dias
#    return total_contagiadoscovid

Contagiados_covid= lambda C,D: C * (2**D)
#Esta funcion halla la cantidad de kilos que hay entre tres animales segun su peso
#Argumentos:
# C(int): cantidad de contagiados
# D(int): cantidad de dias
# Devolvera el total de contagiados segun hayan transcurrido cierta cantidad de dias
print(Contagiados_covid(569,8))
```
## Punto 2:
- De los retos anteriores seleciones 3 funciones y escribalas con argumentos no definidos (*args).
### Explicacion: ###
- Este tema se me dificulto al moemento de ponerlo en práctica ya que no entendia bien como ejecutarlo, decidi buscar mas ejemplos y una forma en la cual pude ejecutarlo y entendo fu usando len para validr los argumentos no definidos anteriormente. luego hice el mismo procedimiento de colocar el proceso matemático y luego llame la función main para ejecutar.
```
def calcularPerRectán (*args)->float:
    """
    Esta función calcula el perimetro de un rectángulo
    Argumentos:
    base: float
    altura: float
    Devuelve: El calculo de el perimetro de un rectángulo
    """  
    if len(args) == 2: #usamos len para una validación de argumentos
        base, altura = args#le damos que argumentos usaremos
        perímetroRectángulo=(base*2)+(altura*2)
        return perímetroRectángulo

if __name__=="__main__": #funcion principal
    base = float (input("Ingrese la base del rectángulo:"))
    altura = float (input("Ingrese la altura del rectángulo:|"))
    print ("El perímetro del rectángulo es: ", str(calcularPerRectán(base,altura)))
     
```
```
def area_rectangular(*args):
    """
    Esta función calcula el area de un rectángulo
    Argumentos:
    base: float
    altura: float
    Devuelve: El calculo de área de un rectángulo
    """
    if len(args) == 2:# hacemos una validación 
        base, altura = args
        area= base*altura #usamos el debido procedimiento matemático
    return area
if __name__ == "__main__":  #Funcion principal
 a= float(input("Ingresa el valor de la base:"))
 b= float(input("Ingresa el valor de la altura:"))
print("Esta es la area de su rectangulo",str(area_rectangular(a,b)))
```
```
from math import pi#importamos math para usar pi
def calcularAreaCírculo(*args)->float:
   """
    Esta función calcula el area de un circulo
    Argumentos:
    base: float
    pi: float
    Devuelve: El calculo de el area de un circulo
   """
   if len (args) == 2: #validamos los argumentos
    radio, pi =args
   areaCírculo=((pi)*(radio*2))#operación de area
   return areaCírculo

if __name__=="__main__":
    radio = float (input("Ingrese el radio del círculo:"))
    print ("El área del círculo con radio:", radio, "es", str(calcularAreaCírculo(radio,pi)))
```
## Punto 3:
- Escriba una función recursiva para calcular la operación de la potencia.
### Explicación: ### 
- Trate de buscar mas ejmplos para entender como funcionaba y logre captar que es aquella función que se llama dentro de si y con ese concepto trabaje para crear el codigo, use condicionales para devolver las potencias que siempre son iguales gracias a sus exponentes luego la llame a ella misma dandole la indicacion de que multiplicara la base por el exponente menos 1 que es una definición para hallar la potencia.
```
def potencia_recursiva(base:float, exponente:int):
    """
    Esta función calcula una potencia
    Argumentos:
    base: float
    exponente: int #numero que multiplica cierta cantidad de veces
    Devuelve: el resultado de la base elevada a exponente veces
    """
    if exponente==0:# caso base: cualquier numero elevado a o es 1
        return 1
    if exponente== 1:# Cualquier numero elevado a 1 es ese mismo numero
        return base
    else:
        return base*potencia_recursiva(base, exponente-1) #caso recursivo
if __name__ == "__main__":  #Funcion principal
    base= float(input("ingrese el numero base:"))
    exponente= int(input("Ingrese su exponente:"))
    print("Aca esta su resultado:", str(potencia_recursiva(base, exponente)))
```
## Punto 4:
- Utilice la siguiente plantilla de code para contar el tiempo:
```
import timeit #Se importa la libreria a ser utilizada

def fibo(n : int )-> int: #Se define la función base
  i : int = 1
  # Caso base
  n1 : int = 0
  n2 : int = 1
  while(i <= n):
    # Condición
    sumFibo = n1 + n2
    # Actualización
    n1 = n2
    n2 = sumFibo
    i += 1
  return sumFibo #Retorna el resultado

if __name__ == "__main__": #Función principal
  num = int(input("Ingrese numero: ")) #Solicitamos el dato necesario   
  start_time1 = timeit.default_timer() #Sew inicia a contar el tiempo de ejecución
  serieFibo = fibo(num)
  timer1= timeit.default_timer() - start_time1 #Se finaliza de contar el tiempo de ejecución
  print(f"El último número de la serie de Fibonacci hasta {num} es {serieFibo}") #Se imprimen los resultados
print(f"fibo se demoró {timer1} en correr")
```
## Punto 5:
- Crear cuenta en stackoverflow y adjuntar imagen en el repo.

[![image.png](https://i.postimg.cc/jSrGSC1f/image.png)](https://postimg.cc/3dnLLrYr)



## Punto 6:
- Cosas de adultos....ir a linkedin y crear perfil....NO IMPORTA que estén iniciando, si tienen tiempo para redes poco útiles como fb, insta, o tiktok tienen tiempo para crear un perfil mamalon. Dejar enlace en el repo

Mi perfil de linkendin es : https://www.linkedin.com/in/maria-paula-machuca-hortua-a14736272/

