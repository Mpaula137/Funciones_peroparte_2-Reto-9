# Funciones_peroparte_2-Reto-9
Realizaremos los ejercicios impuestos en clase que ayudaras a entender como usar lambdas, funciones sin argumento etc.
## Punto 1:
- De los retos anteriores seleciones 3 funciones y escribalas en forma de lambdas.
### Explicación: ###
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
