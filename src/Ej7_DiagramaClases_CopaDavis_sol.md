# Ejercicio 7: Diagrama de Clases - Copa Davis de Tenis

## Descripción del Problema

La Federación Internacional de Tenis necesita un sistema para gestionar la Copa Davis, una competición por equipos entre países. El sistema debe controlar equipos, jugadores, eliminatorias, partidos (individuales y dobles) y resultados.

```plantuml
@startuml 

class Equipo {
  - nombre: String
  - pais: String
  + obtenerJugadores(): List
  + esAnfitrion(): boolean
}

class Jugador {
  - nombreCompleto: String
  - rankingMundial: Int
  - fechaNacimiento: LocalDate
  - nacionalidad: String
}

class Eliminatoria {
  - numero: Int
  - superficie: String
  - equipoAnfitrion: Equipo
  + obtenerGanador(): Equipo
  + obtenerResultadoFinal(): String
}

abstract class Partido {
  - numeroPartido: Int
  - fecha: LocalDate
  - resultado: String
  + obtenerGanador(): Equipo
}

class PartidoIndividual {
  - jugador1: Jugador
  - jugador2: Jugador
  - marcador: String
}

class PartidoDobles {
  - pareja1: Pareja
  - pareja2: Pareja
  - marcador: String
}

class Pareja {
  - jugador1: Jugador
  - jugador2: Jugador
}

Equipo "2" --> "o*.." Jugador : contiene
Eliminatoria "1" --> "2" Equipo : enfrenta
Eliminatoria "1" --> "5" Partido : contiene
PartidoIndividual --> "2" Jugador : participa
PartidoDobles --> "2" Pareja : participa
Pareja --> "2" Jugador : formada por

@enduml
```