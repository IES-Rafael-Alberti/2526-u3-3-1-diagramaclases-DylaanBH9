[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/HJqBG45V)
# Práctica 3.1: Diagrama de clases

## Identificación de la Actividad
- **ID de la Actividad:** 3.1. Diagrama de clases
- **Módulo:** EDES
- **Unidad de Trabajo:** U3: Diseño y diagramas de clases 
- **Fecha de Creación:** 7/12/25
- **Fecha de Entrega:** 9/12/25
- **Alumno(s):**
    - **Nombre y Apellidos:** Dylan Bauti Huelva
    - **Correo electrónico:** dbauhue1708@g.educaand.es
    - **Iniciales del Alumno/Grupo:** DBH

## Descripción del Problema

En esta práctica se diseñan diagramas de clases UML usando PlantUML. Los ejercicios van desde relaciones simples hasta relaciones más complejas con herencia y asociaciones.

### Objetivos
- Identificar las partes principales de un sistema
- Aprender a usar conceptos de Programación Orientada a Objetos
- Diseñar diagramas UML correctamente
- Usar PlantUML para crear los diagramas

## Ejercicios Realizados

### [Ejercicio 1: Sistema de Libros y Autores](src/Ej1_DiagramaClases_LibrosAutor_sol.puml)
Un autor escribe libros. Se muestra cómo un autor puede tener varios libros.

**Conceptos:** Un autor - varios libros, cálculos automáticos.

### [Ejercicio 2: Sistema de Gestión de Cursos Universitarios](src/Ej2_DiagramaClases_CursosUniversitarios_sol.puml)
Un profesor enseña cursos y los estudiantes se inscriben en los cursos. Se registra cuándo se inscriben y qué nota sacan.

**Conceptos:** Varios a varios, tabla intermedia que guarda datos.

### [Ejercicio 4: Sistema de Gestión Empresarial](src/Ej4_DiagramaClases_GestionEmpresarial_sol.puml)
Estructura de una empresa con empleados, clientes y empresas. Algunos empleados supervisan a otros.

**Conceptos:** Herencia, un empleado responsable supervisa otros, cálculos de salario.

### [Ejercicio 6: Sistema de Biblioteca](src/Ej6_DiagramaClases_Biblioteca_sol.puml)
Gestión de libros que se prestan a socios. Control de devoluciones y multas.

**Conceptos:** Estados de libros, préstamos, multas por retraso.

### [Ejercicio 7: Copa Davis de Tenis](src/Ej7_DiagramaClases_CopaDavis_sol.puml)
Un torneo de tenis entre equipos de diferentes países. Cada equipo tiene jugadores y juega partidos.

**Conceptos:** Herencia en partidos, equipos y jugadores, parejas en dobles.

## Instrucciones de Compilación y Ejecución

### Lo que Necesitas
- PlantUML (opcional) o una página web
- Un editor de texto como VS Code
- Extensión PlantUML para VS Code (opcional)

### Cómo Ver los Diagramas

**Opción 1: Con VS Code (la más fácil)**
```bash
# Instala la extensión "PlantUML Official"
# Abre un archivo .puml y presiona Alt+D
```

**Opción 2: En internet sin instalar nada**
```bash
# Copia el contenido en:
# https://plantuml.com/plantuml/uml/
```

## Desarrollo de la Actividad

### Pasos Seguidos

Para cada ejercicio se hizo lo siguiente:
- Leer lo que pidió el cliente
- Encontrar los elementos principales (clases)
- Definir qué datos tiene cada clase
- Definir qué acciones puede hacer cada clase
- Dibujar las conexiones entre clases
- Indicar cuántas unidades se relacionan (uno a uno, uno a muchos, etc.)

### Archivos Creados

| Archivo | Qué es |
|---------|--------|
| `src/Ej1_DiagramaClases_LibrosAutor_sol.puml` | Autor y Libros |
| `src/Ej2_DiagramaClases_CursosUniversitarios_sol.puml` | Profesor, Curso y Estudiante |
| `src/Ej4_DiagramaClases_GestionEmpresarial_sol.puml` | Estructura empresarial |
| `src/Ej6_DiagramaClases_Biblioteca_sol.puml` | Libros y Préstamos |
| `src/Ej7_DiagramaClases_CopaDavis_sol.puml` | Torneo de Tenis |

### Conceptos Clave Aplicados

✓ **Herencia:** Cuando una clase es un tipo especial de otra (en ejercicios 4 y 7)
✓ **Tabla Intermedia:** Para guardar datos cuando dos clases se relacionan (ejercicio 2)
✓ **Cálculos Automáticos:** Datos que se calculan solos a partir de otros
✓ **Cuántas Relaciones:** Especificar si es uno a uno, uno a muchos, etc.
✓ **Público y Privado:** Marcar qué se ve desde fuera y qué es interno
✓ **Relaciones Reflexivas:** Un empleado supervisa a otros empleados

## Resultados de Pruebas

Se verificó que los diagramas sean correctos:
- ✓ Todas las partes principales están incluidas
- ✓ Los datos tienen el tipo correcto
- ✓ Los cálculos automáticos están marcados
- ✓ Las cantidades de relaciones son correctas
- ✓ El código PlantUML funciona bien

## Conclusiones

Se crearon correctamente los diagramas de clases para diferentes sistemas. Los diagramas muestran cómo las clases se relacionan entre sí y qué hace cada una.

### Lecciones Aprendidas
- Cómo identificar bien las cantidades en las relaciones
- Cuándo usar una tabla intermedia para guardar datos
- Cómo usar herencia cuando una clase es un tipo de otra
- Cómo documentar datos calculados automáticamente

## Referencias y Fuentes

- [PlantUML - Documentación](https://plantuml.com/)
- [Diagramas UML - Tutoriales](https://www.uml-diagrams.org/)
- Los archivos .md con los requisitos originales

---

**Repositorio:** [GitHub - 2526-u3-3-1-diagramaclases](https://github.com/IES-Rafael-Alberti/2526-u3-3-1-diagramaclases-DylaanBH9)