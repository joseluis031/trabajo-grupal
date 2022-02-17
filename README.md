# trabajo-grupal

La direccion de GitHub de este repositorio es: [GitHub](https://github.com/joseluis031/trabajo-grupal.git)

## Ejercicio 1
```
tipo DIA estructura
    # Versión 1
    (lunes, martes, miércoles, jueves, viernes, sábado, domingo)
fin DIA

tipo DIA estructura
    # versión 2
    # (lunes, martes, miércoles, jueves, viernes, sábado, domingo)
      (  1,     2,      3,       4,      5,        6,      0    )
fin DIA
```
## Ejericico 2

Algoritmo 2: Otra definición de sucesor por enumeración
```
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

## Ejercicio 7

Algoritmo Ej7_Viaje_Escolar
```
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
