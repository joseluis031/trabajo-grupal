# trabajo-grupal

La direccion de GitHub de este repositorio es: [GitHub](https://github.com/joseluis031/trabajo-grupal.git)

## Ejercicio 1

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

