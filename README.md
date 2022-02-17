# trabajo-grupal

La direccion de GitHub de este repositorio es: [GitHub](https://github.com/joseluis031/trabajo-grupal.git)

## Ejercicio 1

tipo DIA estructura
    # Versión 1
    (lunes, martes, miércoles, jueves, viernes, sábado, domingo)
fin DIA


```
Algoritmo 2: Otra definición de sucesor por enumeración

sucesor(día : DIA) : DIA
    # El sucesor de `día' en la semana.

Realización
    siguiendo el valor de día hacer
        = 'lunes' :
            Resultado ← 'martes'
        = 'martes' :
            Resultado ← 'miércoles'
        = 'miércoles' :
            Resultado ← 'jueves'
        = 'jueves' :
            Resultado ← 'viernes'
        = 'viernes' :
            Resultado ← 'sábado'
        = 'sábado' :
            Resultado ← 'domingo'
        = 'domingo' :
            Resultado ← 'lunes'
        si no
            Nada
    fin hacer
    
postcondición
    día = 'lunes' => Resultado = 'martes'
    día = 'martes' => Resultado = 'miércoles'
    ...
fin sucesor
```

## Ejercicio 3

```
Cálculo del importe del descuento
 descuento(precio:REAL):REAL
    #Importe del descuento acordado sobre 'precio'.
    
 Precondición
    precio <= 0
    
 Realización
    si 
        precio < 100,00
    entonces
        # precio < 100,00 => no hay descuento
        Resultado ← 0,00
    si no si 
        precio < 500
    entonces
        # 100 =< precio < 500 => descuento del 5%
        Resultado ← precio x0,08
    fin si

Postcondición
    precio < 100,00 => Resultado = 0,00
    100 =< precio < 500 => Resultado = precio x0,05
    500 =< precio => Resultado = precio x0,08
    
fin descuento         
```

## Ejercicio 6
```
Algoritmo Descuento_microprocesadores
	
	//Definimos las variables
	Definir componentes_pedidos Como Entero
	Definir tipo_cliente Como Caracter
	Definir descuento Como Real
	
	//Introducimos los valores de las variables por teclado
	Escribir "¿Cuantos componentes se han pedido? "
	Leer componentes_pedidos
	Escribir "Tipo de cliente: "
	Leer tipo_cliente
	
	//Primer bucle para calcular el descuento
	Si componentes_pedidos < 10000 Entonces
		descuento<-0.00
	SiNo
		Si 10000 <= componentes_pedidos y componentes_pedidos <= 20000 Entonces
			descuento<-0.10
		SiNo
			Si componentes_pedidos > 20000 y componentes_pedidos <= 40000 Entonces
				descuento<-0.15
			SiNo
				descuento<-0.20
			FinSi
		FinSi
	FinSi
	
	//Segundo bucle para calcular el descuento
	Si tipo_cliente = "COMMAQ" Entonces
		descuento<-descuento-0.02
	Sino 
		Si tipo_cliente = "BEL" Entonces
			descuento<-descuento+0.01
		FinSi
	FinSi
	
	//Mostramos el descuento por pantalla
	Escribir "Su descuento es la friolera de ", descuento, "%"
	
FinAlgoritmo
```

## Ejercicio 7
```
Algoritmo Viaje_Escolar

	//Definimos las variables
	Definir numero_alumnos, numero_dias Como Entero
	Definir alojamiento, coste_alumno, coste_por_alumno, coste_final Como Real
	Escribir "Escriba el numero de alumnos y el numero de dias: "
	Leer numero_alumnos, numero_dias
	
	coste_comida<-3.50*numero_dias
	
	//Bucle para hallar el coste del alumno
	Si numero_alumnos > 25 Entonces
		coste_alumno<-61.00
	SiNo
		coste_alumno<-67.30
	FinSi
	
	//Bucle para calcular el alojamiento
	Si numero_alumnos < 30 Entonces
		alojamiento<-4.75*numero_dias
	SiNo
		Si 31 <= numero_alumnos y numero_alumnos <= 35 Entonces
			alojamiento<-4.00*numero_dias
		SiNo
			alojamiento<-3.50*numero_dias
		FinSi
	FinSi
	
	coste_por_alumno<-coste_alumno + alojamiento
	coste_final<-coste_por_alumno * numero_alumnos
	
	//Mostramos el precio del coste por alumno y el coste total por pantalla
	Escribir coste_por_alumno
	Escribir coste_final
	
FinAlgoritmo
```
## Ejercicio 8
```
Algoritmo prima_anual

Algoritmo prima_anual
#Impporte de la prima anual en función del número de accidentes, de la distancia
#recorrida y de la antigüedad del conductor.

Entrada
	accidentes : ENTERO # Número de accidentes
	distancia : ENTERO # Distancia recorrida
	Antigüedad : ENTERO # Antigüedad
	
Resultado: REAL

Variable
	prima_antigüedad:REAL
	prima_distancia:REAL
	
Realización
	si
		accidentes > 3
	entonces
		Resultado ← 0,00
	si no 
		#Calculo de la prima de antigüedad
		si
			antigüedad < 4
		entonces 
			prima_antigüedad ← 200,00 + REAL(antigüedad - 4)x20,00
		fin si
		#Cálculo de la prima de rendimiento
		prima_distancia ← inf (REAL(distancia)x0,01,REAL(400))
		#Cálculo de la prima anual
		Resultado ← (prima_antigüedad + prima_distancia)/REAL(accidentes + 1)
	fin si
	
Postcondición
...

fin prima_anual
```
