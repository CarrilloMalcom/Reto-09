# Reto-09

### Soy Malcom Yamil Carrillo Quintero y pertenezco al grupo de "Fenomenoides", adelante se muestra nuestro logo
<details><summary>Preparense para ver el grandioso logo: </summary><p>
<div align='center'>
<figure> <img src="https://i.postimg.cc/NFbwf57S/logo-def.png" alt="Defensa Civil" width="400" height="auto"/></br>
<figcaption><b> "somos programadores, no diseñadores" </b></figcaption></figure>
</div>
</p></details><br>


## 1.
### De los retos anteriores selecione 3 funciones y escribalas en forma de lambdas.

``` python
import math # importa el paquete math
p=math.pi # p se inicializa como math.pi que es p traido por el paquete math
if __name__=="__main__":
    r1=float(input("Ingrese el radio de la esfera: ")) # r1 es un entero proveniente de entrada de teclado
    r2=float(input("Ingrese el radio del cono: ")) # r2 es un entero proveniente de entrada de teclado
    h=float(input("Ingrese la altura: ")) # h es un entero proveniente de entrada de teclado
    calcular_SA=lambda r1,r2,h: (4*p*(r1**2))+(p*r2*((h**2)+(r2**2))**0.5)+(p*(r2**2)) # calcular_SA es una función la cual es 4π(r1)^π(r2)+(π(r2)(√(h^2+(r2)^2)))+(π(r2)^2)
    calcular_V= lambda r1,r2,h: ((4/3)*p*(r1**3))+((1/3)*p*(r2**2)*h) # calcular_V es una función la cual es 4/3π(r1)^3 + 1/3π(r2)^2*h
    Area=calcular_SA(r1,r2,h) # Area es igual al retono de la función calcular_SA con los argumentos r1,r2,h
    Volumen=calcular_V(r1,r2,h) # Volumen es igual al retorno de la función calcular_V con los argumentos r1,r2,h
    print(f"El área superficial del solido es {Area} y el volumen es {Volumen}") # imprimir "El área superficial del solido es Area y el volumen es Volumen"
```
> Función para calcular el area superficial y el volumen de una figura consistente de una esfera y un cono  
``` python
import math # importa el paquete math
p=math.pi # p se inicializa como math.pi que es p traido por el paquete math
if __name__ =="__main__":
    r=float(input("Ingrese el radio de los circulos: ")) # r es un flotante o real proveniente de entrada de teclado
    b=float(input("Ingrese el ancho del rectangulo: ")) # b es un flotante o real proveniente de entrada de teclado
    a=float(input("Ingrese la altura del rectangulo: ")) # a es un flotante o real proveniente de entrada de teclado
    calcular_A= lambda r,b,a: (2*(p*(r**2)))+(b*a) # calcular_A es una función igual a (2(πr^2))+(b*a)
    calcular_P=lambda r,b,a: (2*(2*p*r))+((2*a)+(2*b)) #calcular_P es una función igual a (2(2πr))+(2a)+(2b)
    Ar=calcular_A(r, b, a) #Ar es igual al retorno de la función calcular_A con los argumentos r,b,a
    Per=calcular_P(r,b, a) #Per es igual al retorno de la función calcular_P con los argumentos r,b,a
    print(f"El area de la figura es {Ar} y el perimetro es {Per}") # imprimir "El area de la figura es Ar y el perimetro es Per"
```
>Función para calcular el area y el perimetro de una figura consistente de dos circulos iguales y un rectangulo
``` python
p:int=300 # p se define como un entero igual 300
m:int=3300 # m se define como un entero igual 3300
h:int=350 # h se define como un entero igual 350
if __name__=="__main__":
    P=int(input("Ingrese la cantidad de panes que le mandaron a comprar: ")) # P es un entero proveniente de entrada de teclado
    M=int(input("Ingrese la cantidad de bolsas de leche que le mandaron a comprar: ")) # M es un entero proveniente de entrada de teclado
    H=int(input("Ingrese la cantidad de huevos que le mandaron a comprar: ")) # H es un entero proveniente de entrada de teclado
    B=int(input("Ingrese la cantidad de dinero que le dieron (Pesos): ")) # B es un entero proveniente de entrada de teclado
    calcular_vueltas= lambda P,M,H,B:B-((P*p)+(M*m)+(H*h)) # calcular_vueltas es una función igual a B-(Pp+Mm+Hh)
    Residuo=calcular_vueltas(P,M,H,B) # Residuo es igual al retorno de la función calcular_vueltas con los argumentos P,H,M,B
    if Residuo>0: # si Residuo es mayor a 0
        print(f"Las vueltas de su compra son {Residuo} pesos") # imprimir "Las vueltas de su compra son Residuo pesos"
    else:# si no
        Residuo=Residuo*(-1) # Residuo es igual a Residuo*-1
        print(f"Le hacen falta {Residuo} pesos para su compra") #imprimir "Le hacen falta Residuo pesos para su compra"
```
> Calcular vueltas o el dinero faltante de una compra de huevos, pan y bolsas de leche, dada la cantidad de cada producto y el dinero con el que se va a comprar

## 2.
### De los retos anteriores selecione 3 funciones y escribalas con argumentos no definidos (*args).
``` python
n:int=1 # n se define como un entero igual 1
m:int=7 # m se define como un entero igual 7
k:int=6 # k se define como un entero igual 6
def carne_de_ave(*args)->int: # se inicia la función carne_de_ave con argumentos no definidos
    Nkg=args[0]*n # Nkg es igual al primer argumento multiplicado por n
    Mkg=args[1]*m # Mkg es igual al segundo argumento multiplicado por m
    Kkg=args[2]*k # Kkg es igual al tercer argumento multiplicado por ñ
    return Nkg+Mkg+Kkg # la función retorna Nkg+Mkg+Kkg

if __name__=="__main__":
    N=int(input("Ingrese la cantidad de gallinas: ")) # N es un entero proveniente de entrada de teclado
    M=int(input("Ingrese la cantidad de gallos: ")) # M es un entero proveniente de entrada de teclado
    K=int(input("Ingrese la cantidad de pollitos: ")) # K es un entero proveniente de entrada de teclado
    carne=carne_de_ave(N,M,K) # carne es igual al retorno de la función carne_de_ave con los argumentos N,M,K
    print(f"La cantidad de carne de aves es igual a {carne} kg") # imprimir "La cantidad de carne de aves es igual a carne kg"
```
> Función para el calculo de la cantidad de carne de aves en kg  
``` python
def calcular_prestamo(*args)->int: # se inicia la función calcular_prestamo con argumentos no definidos
    return args[0]*((1+(args[1]/100))**args[2]) # la función retorna args[0]*((1+(args[1]/100))**args[2])

def calcular_prestalt(*args)->int: # se inicia la función calcular_prestalt con argumentos no definidos
    prest=args[0] #prest es igual al primer argumento
    for j in range(args[2]): # para j en rango del tercer argumento
        prest=prest+(prest*(args[1]/100)) # prest es igual a prest+(prest*(segundo argumento/100))
    return prest

if __name__=="__main__":
    C=int(input("Ingrese el valor base del prestamo: ")) # C es un entero proveniente de entrada de teclado
    i=int(input("Ingrese el valor del interés: ")) # i es un entero proveniente de entrada de teclado
    n=int(input("Ingrese la cantidad de meses para el valor del prestamo: ")) # n es un entero proveniente de entrada de teclado
    P=calcular_prestamo(C,i,n) #P es igual al retorno de la función calcular_prestamo con los argumentos C,i,n
    Palt=calcular_prestalt(C,i,n) #Palt es igual al retorno de la función calcular_prestalt con los argumentos C,i,n
    print(f"El valor del prestamo es {P} \n El valor es {Palt}") # imprimir "El valor del prestamo es {P} \n El valor es {Palt}"
```
>Calculo del valor de un prestamo con interés compuesto
``` python
def numero_contagiados(*args)->int: # se inicia la función numero_contagiados con argumentos no definidos
    cont=args[1] # cont es igual al segundo argumento
    for j in range (args[0]): # para j en rango del primer argumento
        cont=cont*2 # cont es igual a cont*2
    return cont # retornar cont 

if __name__ =="__main__":
    C=int(input("Ingrese el numero actual de contagiados: ")) # C es un entero proveniente de entrada de teclado
    D=int(input("Ingrese el numero de dias para la predicción de contagiados: ")) # D es un entero proveniente de entrada de teclado
    cont=numero_contagiados(D, C) #cont es igual al retorno de la función numero_contagiados con los argumentos C,D
    print(f"El numero de contagiados dentro de {D} dias si el numero actual son {C} contagiados serán {cont}") #imprimir "El numero de contagiados dentro de D dias si el numero actual son C contagiados serán cont"
```
> Numero de contagiados de COVID-19 de nuncalandia si la cantidad se duplica cada día, dada la cantidad de dias y la cantidad de contagiados inicial


## 3.
## Escriba una función recursiva para calcular la operación de la potencia.

``` python
r:int=1 # r se inicializa como un entero igual a 1
def potencia (b:int, p:int, r:int)->int: # se inicia la función potencia con los argumentos b, p, r
    if p<1: # si p es menor a 1
        return r #retornar r
    else: # si no
        r*=b # r es igual a r*b
        p -= 1 # p es igual a p-1
        return potencia(b, p, r) #retornar a la función potencia con los argumentos b, p, r
    
if __name__=="__main__":
    b=int(input("Ingrese la base de su potencia: ")) # b es un entero proveniente de entrada de teclado
    p=int(input("Ingrese el exponente de su potencia: ")) # p es un entero proveniente de entrada de teclado
    R=potencia(b, p, r) # R es igual al retorno de la función potencia con los argumentos p, b, r
    print(f"El resultado de {b}^{p} es igual a {R}") # imprimir "El resultado de b^p es igual a R"
```

## 4. 
### Comparación de tiempo de ejecución función para n numeros de la serie de fibonacci con función con un ciclo y una función recursiva
``` python
import time # importar el paquete time
def Fibonacci(n: int) -> int: # se inicia la función Fibonacci con los argumentos n
  n1 = 0 # n1 es igual a 0
  n2 = 1 # n2 es igual a 1
  for i in range(n): # para i en rango de n
    fibo = n1 + n2 # fibo es igual a n1+n2
    n1 = n2 # n1 se actualiza como n2
    n2 = fibo# n2 se actualiza como fibo
  return fibo # retornar fibo

def fiboRecursivo(n : int )-> int: # se inicia la función fiboRecursivo con los argumentos n
  if n <=1: # si n es menor o igual a 1
    return 1 # retornar 1
  else: # si no
    return fiboRecursivo(n-1)+fiboRecursivo(n-2) # retornar la suma del retorno de la función fiboRecursivo con argumento n-1 y la función fiboRecursivo con argumento n-2

if __name__ == "__main__":
  n = int(input("Ingrese la cantidad de numeros que quiere para la secuencia de fibonacci: ")) # n es igual a un entero proveniente de entrada de teclado
  start1_time = time.time() # start1_time es igual time.time es decir al tiempo en el que se define
  Fibo = Fibonacci(n) # Fibo es igual al retorno de la función Fibonacci con el argumento n
  print(f"la serie de fibonacci con {n} numeros llega hasta {Fibo}") # imprimir la serie de fibonacci con n numeros llega hasta Fibo
  end1_time = time.time() # end1_time es igual time.time es decir al tiempo en el que se define
  ttime1=end1_time-start1_time #ttime1 es igual a la resta de end1_time menos start1_time

  start2_time = time.time() # start1_time es igual time.time es decir al tiempo en el que se define
  Fibo = fiboRecursivo(n) # Fibo es igual al retorno de la función fiboRecursivo con el argumento n 
  print(f"la serie de fibonacci con {n} numeros llega hasta {Fibo}") # imprimir la serie de fibonacci con n numeros llega hasta Fibo
  end2_time = time.time() # start1_time es igual time.time es decir al tiempo en el que se define
  ttime2=end2_time-start2_time #ttime1 es igual a la resta de end1_time menos start1_time

  if ttime1<ttime2: # si ttime1 es mayor a ttime 2
    print(f"El proceso más rapido fue el de la función no recursiva con {n} numeros de la secuencia \nLa diferencia fue de {ttime2-ttime1}") # imprimir "El proceso más rapido fue el de la función no recursiva con n numeros de la secuencia \nLa diferencia fue de ttime2-ttime1"
  elif ttime1>ttime2: # si ttime1 es menor a ttime 2
    print(f"El proceso más rapido fue el de la función recursiva con {n} numeros de la secuencia \nLa diferencia fue de {ttime1-ttime2}") # imprimir "El proceso más rapido fue el de la función recursiva con n numeros de la secuencia \nLa diferencia fue de ttime1-ttime2")
  else: # de otra manera
    print("Las 2 funciones tomaron lo mismo") # imprimir "Las 2 funciones tomaron lo mismo"
  print(f"Función no recursiva: {ttime1} Función recursiva: {ttime2}") #imprimir "Función no recursiva: ttime1 Función recursiva: ttime2"
```

## 5. 
<figure> <img src="https://i.postimg.cc/Xq0cZJ1m/Stack-overflow.png" alt="Defensa Civil" width="400" height="auto"/></br>

## 6.

### Cosas de adultos... ya hay perfil de [LinkedIn](https://www.linkedin.com/in/malcom-yamil-carrillo-quintero-a0a85a2b1/)
