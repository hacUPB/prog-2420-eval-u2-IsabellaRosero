[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/fz23fUQP)
# Documentación del proyecto
## Unidad 2

Estudiante: Isabella Rosero 
ID:  000505216
---
# Autoevaluación
## Nota: 4.2


# Pseudocodigos y análisis:
## Problema 1
### Pseudocodigo

Inicio

1. Información del usuario
Solicitar titulo (Sr. o Sra)
Solicitar nombre
Solicitar apellido

2. Imprimir saludo personalizado "
Imprimir "Bienvenido a FastFast Airlines, "+Titulo+""+nombre+""+apellido+""

3. Seleccion de destino de vuelo
Solicitar origen (Medellín, Bogotá, Cartagena)
Imprimir Menú de origen (Medellín, Bogotá, Cartagena)
Solicitar destino (Medellín, Bogotá, Cartagena)
Imprimir Menú de destino (Medellín, Bogotá, Cartagena)
Solicitar dia de la semana (Lunes, Martes, Mierecoles, Jueves, Vierenes, Sabado, Domingo)
Imprimir menú de dias de la semana 
Solicitar día del mes con un rango de (1-30)

4. Calcular la distancia entre ciudades 
SI origen = "Medellin" y destino = "Bogota"
  distancia = 240
SI NO SI origen = "Medelllin" y destino = "Cartagena"
  distancia = 461
SI NO SI origen = "Bogota" y destino = "Cartagena"
  distancia = 657

5. Calcular el precio del boleto 
SI distancia <400
  SI día de la semana = "Lunes" O día de la semana = "Martes" O día de la semana = "Miércoles" O día de la semana = "Jueves"
   Precio = 79.900

SI NO
   Precio = 119.900

SI NO 
  SI día de la semana = "Lunes" O día de la semana = "Martes" O día de la semana = "Miércoles" O día de la semana = "Jueves"

   Precio = 156.900

SI NO
   Precio = 213.000

6. Número de asiento
Solicitar preferencia del asiento (Pasillo, Ventana, Sin preferencia)
Imprimir menú de preferencia de asiento 

SI preferencia = "pasillo"
    asiento = "C"
SINO SI preferencia = "ventana"
    asiento = "A"
SINO
    asiento = "B"

7. Seleciionar numero de asiento
 numero de asiento = ALEATORIO de (1,29)

8. Salida
Imprimir "Nombre completo: " + título + " " + nombre + " " + apellido
Imprimir "Origen: " + origen
Imprimir"Destino: " + destino
Imprimir "Fecha de vuelo: " + día de la semana + " " + día del mes
Imprimir "Precio del boleto: " + precio
Imprimir "Asiento asignado: " + número de asiento + asiento

FIN

### Análisis
Este sistema de reservas de aerolíneas tiene como objetivo principal permitir que los usuarios puedan reservar vuelos de manera sencilla y eficiente. Para lograr esto, el programa necesita recopilar la información personal del usuario, como su nombre completo y preferencia de asiento, y luego permitirle seleccionar un vuelo entre varias opciones de origen y destino.

Una vez que el usuario ha ingresado su información y ha seleccionado un vuelo, el sistema se encarga de calcular el precio del boleto. Este cálculo se basa en la distancia entre las ciudades y en el día de la semana en que el usuario desea viajar. Es interesante notar que hay reglas específicas para determinar el precio, lo que significa que el sistema tiene que tener una lógica interna clara para poder calcular estos precios de manera precisa.

Además de calcular el precio, el sistema también asigna un asiento al usuario. Esto no es solo una asignación aleatoria, ya que el programa toma en cuenta las preferencias del usuario, como si prefiere un asiento en el pasillo, junto a la ventana, o si no tiene ninguna preferencia. Esto hace que la experiencia del usuario sea más personalizada y satisfactoria.

Una vez que toda la información ha sido recopilada y procesada, el sistema presenta un resumen final al usuario. Este resumen incluye el nombre completo del usuario, el vuelo seleccionado, el precio del boleto y el asiento asignado. Este paso es crucial porque le confirma al usuario que su reserva se ha completado correctamente y le proporciona todos los detalles que necesita para su viaje.

## Problema 2
### Pseudocodigo

INICIO

1. Pedir datos de entrada
PEDIR altitud_inicial (en kilómetros)
PEDIR coeficiente_arrastre (un valor decimal pequeño, como 0.01)
PEDIR altitud_minima_seguridad (en kilómetros)

2. Inicializar variables
altitud_actual = altitud_inicial
coeficiente_arrastre_actual = coeficiente_arrastre

3. imulación de desintegración orbital
MIENTRAS altitud_actual > altitud_minima_seguridad

}Calcular pérdida de altitud debido al arrastre
    altitud_perdida = coeficiente_arrastre_actual * altitud_actual
    altitud_actual = altitud_perdida

Aumentar coeficiente de arrastre
    coeficiente_arrastre_actual += 0.0001

Mostrar estado actual
    MOSTRAR "Altitud actual: " + altitud_actual + " km"
    MOSTRAR "Coeficiente de arrastre actual: " + coeficiente_arrastre_actual

Detener si se estabiliza
    SI altitud_perdida < 0.1
        ROMPER

4. Mostrar resultado final
SI altitud_actual <= altitud_minima_seguridad

    MOSTRAR "El satélite ha reingresado en la atmósfera terrestre y se ha desintegrado."
   
SINO
    MOSTRAR "El satélite se ha estabilizado en una órbita baja."

FIN

### Análisis

Este programa simula cómo un satélite en órbita pierde altitud debido al arrastre atmosférico y eventualmente podría reingresar en la atmósfera terrestre o estabilizarse en una órbita baja. Al principio, el programa le pide al usuario que ingrese algunos datos: la altitud inicial del satélite, un valor pequeño que representa el arrastre atmosférico, y una altitud mínima de seguridad, que es el límite por debajo del cual el satélite ya no se considera seguro en órbita.

Una vez que se tienen estos datos, el programa comienza con la simulación. La altitud del satélite se va actualizando en cada paso, restando la pérdida de altitud causada por el arrastre. Este arrastre se hace más fuerte a medida que el satélite desciende, por lo que el programa también incrementa el valor del coeficiente de arrastre en cada paso. El programa sigue simulando este proceso hasta que el satélite alcanza la altitud mínima de seguridad o hasta que la pérdida de altitud se vuelve muy pequeña, lo que indicaría que el satélite se ha estabilizado.

Finalmente, el programa verifica en qué estado quedó el satélite. Si ha caído por debajo de la altitud mínima, muestra un mensaje indicando que el satélite ha reingresado en la atmósfera y se ha desintegrado. Si, por otro lado, el satélite no descendió tanto y la pérdida de altitud se estabilizó, el programa indica que el satélite ha alcanzado una órbita baja estable
