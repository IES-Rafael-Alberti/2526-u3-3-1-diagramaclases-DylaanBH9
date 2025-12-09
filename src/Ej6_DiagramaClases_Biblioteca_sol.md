# Ejercicio 6: Diagrama de Clases - Sistema de Biblioteca

## Descripción del Problema

Una biblioteca municipal necesita informatizar su sistema de gestión de libros y préstamos. El sistema debe controlar el catálogo de libros, los autores, los socios lectores y el estado de cada préstamo.

```plantuml
@startuml 

class Autor {
  - nombreCompleto: String
  - fechaNacimiento: LocalDate
  + obtenerEdad(): int {derived}
}

class Libro {
  - titulo: String
  - isbn: String
  - tipo: String
  - estado: String
}

class Socio {
  - nombre: String
  - dni: String
  - fechaInscripcion: LocalDate
  + prestarLibro(): boolean
  + devolverLibro(): boolean
  + obtenerLibrosPrestados(): Int
  + tieneMultaActiva(): boolean
}

class Prestamo {
  - fechaPrestamo: Date
  - fechaLimite: Date {derived}
  + calcularFechaLimite(): LocalDate
  + verificarRetraso(): boolean
}

class Multa {
  - fechaInicio: LocalDate
  - diasMulta: Int
  + estaActiva(): boolean
}

Autor "1..*" --> "o*.." Libro : escribe
Socio "1" --> "o*.." Prestamo : realiza
Libro "1" --> "o*.." Prestamo : puede ser

@enduml
```