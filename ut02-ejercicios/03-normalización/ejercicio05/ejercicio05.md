# Ejercicio 5

En una universidad, se lleva un registro de cursos, estudiantes y sus calificaciones. Sin embargo, la tabla CursosEstudiantes no está completamente normalizada.

Normaliza la tabla CursosEstudiantes para que cumpla con 1FN, 2FN y 3FN. Identifica las dependencias funcionales y elimina las dependencias parciales y transitivas en cada paso.

| RegistroID | EstudianteID | NombreEstudiante | Cursos | Profesor | Notas | Departamento |
| ---------- | ------------ | ---------------- | ------ | -------- | ----- | ------------ |
| 1 | 201 | Alicia | "Matemáticas, Física" | "Dr. Pérez" | "85, 90" | Ciencias |
| 2 | 202 |	Roberto | "Matemáticas, Química" | "Dr. Pérez" | "78, 88" | Ciencias |
| 3 | 203 |	Julia |	"Historia, Literatura" | "Dr. Gómez" | "92, 80" | Humanidades |
| 4 | 204 |	Mario |	"Química" |	"Dr. Pérez" | "75" | Ciencias |

## Resolución

Tabla `profesores`

| Profesor | Departamento | 
| -------- | ------------ |
| "Dr. Pérez" | Ciencias |
| "Dr. Pérez" | Humanidades |

Tabla `alumnos`

| RegistroID | EstudianteID | NombreEstudiante |
| ---------- | ------------ | ---------------- |
| 1 | 201 | Alicia |
| 2 | 202 | Roberto |
| 3 | 203 | Julia |
| 4 | 204 | Mario |

Tabla `cursos`

| Curso | Profesor |
| ----- | -------- |
| Matemáticas | "Dr. Pérez" |
| Física | "Dr. Pérez" |
| Química | "Dr. Pérez" |
| Historia | "Dr. Gómez" |
| Literatura |  "Dr. Gómez" |s

Tabla `cursos-alumnos`

| EstudianteID | Notas | Curso |
| ------------ | ----- | ----- |
| 201 | 85 | Matemáticas |
| 201 | 90 | Física |
| 202 | 78 | Matemáticas |
| 202 | 88 | Química |
| 203 | 92 | Historia |
| 203 | 80 | Literatura |
| 204 | 75 | Química |