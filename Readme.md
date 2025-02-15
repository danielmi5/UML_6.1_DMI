# Actividad Casos de uso 6.1
## 1. Crea el diagrama de uso haciendo uso de platuml, representado los actores y casos de uso que identifiques en los requisitos.
```
@startuml

:Cliente: as C
(validarse) as va
C --> va
(Sacar_dinero) as sd
C --> sd
sd ..> va : include
(Hacer_transferencia) as ht
C --> ht 
ht ..> va : include
(Realizar_ingreso) as ri
C --> ri
ri ..> va : include

(Saldo_insuficiente) as si
si ...> sd : extend
si ...> ht : extend
(Limite_diario) as ld
ld ..> sd : extend

@enduml
```

## 2. Describe, haciendo uso de la plantilla, al menos el caso de uso "Sacar dinero", con las interacciones que tiene entre el actor y el caso de uso.

##### Caso 1 -> Validación 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente debe autenticarse para realizar cualquier operación en el cajero.

##### Caso 2 -> Sacar dinero 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede sacar dinero de su cuenta, pero antes debe haberse validado. A menos que, no tenga saldo o supere el límite diario.

##### Caso 3 -> Transferencia 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede hacer una transferencia a otra cuenta, pero antes debe haberse validado. A menos que, se haya quedado sin saldo.

##### Caso 4 -> Realizar ingreso
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede hacer un ingreso a través del cajero, pero antes debe haberse validado.


## 3. Responde a las siguiente pregunta:¿Para qué me sirve tener/realizar un diagrama de casos de uso modelando el sistema que se representa? ¿Qué aporta?

Un diagrama de casos de uso permite visualizar, de manera clara y estructurada, cómo los distintos actores interactúan con el sistema. Se usan principalmente para: 

- Definir requisitos funcionales.
- Identificar con claridad las funciones del sistema. 
- Conocer cuáles y cuántos actores participan, además de sus casos de uso.
- Facilitan la documentación y el análisis.

Especifican qué debe hacer el sistema, mejoran la comunicación facilitan el entendimiento entre clientes y desarrolladores. Además, ayudan a estructurar mejor la arquitectura del software. En resumen, aportan orden, claridad y eficiencia al proceso de desarrollo.



