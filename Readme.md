# Actividad Casos de uso 6.1
## Código plantuml
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
si ...> ri : extend
(Limite_diario) as ld
ld ..> sd : extend
ld ..> ht : extend
ld ..> ri : extend

@enduml
```

## Detalles

##### Caso 1 -> Validación 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente debe autenticarse para realizar cualquier operación en el cajero.

##### Caso 2 -> Sacar dinero 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede sacar dinero de su cuenta. A menos que, no tenga saldo o supere el límite diario.

##### Caso 3 -> Transferencia 
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede hacer una transferencia a otra cuenta. 

##### Caso 4 -> Realizar ingreso
- **Actor:** Cliente
- **Sistema:** Cajero
- **Descripción:** El cliente puede hacer un ingreso a través del cajero.

