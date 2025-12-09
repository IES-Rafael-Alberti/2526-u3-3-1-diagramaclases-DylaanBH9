# Ejercicio 4: Diagrama de Clases - Sistema de Gestión Empresarial

## Descripción del Problema

Una empresa de consultoría necesita desarrollar un sistema para gestionar la información de sus empleados, clientes y las empresas con las que trabajan. El sistema debe mantener datos personales, estructuras jerárquicas y relaciones comerciales entre las diferentes entidades.

```plantuml
@startuml

abstract class Persona {
  - nombreCompleto: String
  - fechaNacimiento: LocalDate
  + obtenerEdad(): Int {derived}
}

class Empleado{
  - sueldoBruto: Int
  + obtenerSueldoNeto(): Int {derived}
}

class EmpleadoResponsable{
  - categoria: String
}

class Cliente{
  - numeroTelefono: String
}

class Empresa {
  - nombre: String
  - cif: String
  - direccion: String
}

EmpleadoResponsable "1" --> "o*.." Empleado : supervisa
Cliente "o*.." --> "1..*" Empresa : pertenece a

@enduml
```