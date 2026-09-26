# Proyecto: SALUD 360

Este es el repositorio central del sistema de gestión para la clínica. La plataforma maneja el flujo completo de citas, atención en consulta, historial médico y farmacia, desarrollado bajo la metodología Scrum.

# 1. Listado de Actividades
El sistema cubre las siguientes 15 funciones principales:
1. Pedir citas
2. Modificar estado de citas
3. Pago de citas
4. Pago de medicamentos
5. Consultar historias clínicas
6. Registro de usuarios (Pacientes)
7. Registro de profesionales (Médicos)
8. Inicio de sesión
9. Cierre de sesión
10. Consultar disponibilidad de especialistas
11. Consultar y descargar resultados
12. Registrar consulta médica
13. Registrar signos vitales
14. Registro de tratamiento médico
15. Catálogo e inventario de medicamentos



# 2. Product Backlog (Épicas y Features)

# Épica 1: Control de Accesos y Usuarios (Prioridad: Alta)
*Nota: Es la base de seguridad. Necesitamos identificar si ingresa un paciente o un médico antes de dar acceso a agendas o datos protegidos.*
*   Feature 1.1: Registro de Usuarios**
    *   Registro de usuarios (Actividad 6)
    *   Registro de profesionales (Actividad 7)
*   Feature 1.2: Login y Sesión**
    *   Inicio de sesión (Actividad 8)
    *   Cierre de sesión (Actividad 9)

# Épica 2: Agendar y Gestionar Citas (Prioridad: Alta)
*Nota: El motor operativo del día a día para coordinar los horarios de los médicos con los pacientes.*
*   Feature 2.1: Búsqueda y Disponibilidad**
    *   Consultar disponibilidad de especialistas (Actividad 10)
*   Feature 2.2: Flujo de Citas**
    *   Pedir citas (Actividad 1)
    *   Modificar estado de citas (Actividad 2)

# Épica 3: Atención Clínica en Consulta (Prioridad: Media)
*Nota: Módulo donde el médico recopila el estado del paciente y toma decisiones clínicas.*
*   Feature 3.1: Registro en Consulta**
    *   Registrar consulta médica (Actividad 12)
    *   Registrar signos vitales (Actividad 13)

# Épica 4: Tratamientos, Medicamentos y Resultados (Prioridad: Media)
*Nota del equipo: Movimos "Consultar historias clínicas" aquí porque no es solo un dato de usuario, sino el historial médico dinámico que se alimenta de cada consulta y tratamiento.*
*   Feature 4.1: Historial y Diagnósticos**
    *   Consultar historias clínicas (Actividad 5)
    *   Consultar y descargar resultados (Actividad 11)
*   *Feature 4.2: Recetas y Farmacia**
    *   Registro de tratamiento médico (Actividad 14)
    *   Catálogo e inventario de medicamentos (Actividad 15)

# Épica 5: Transacciones y Facturación (Prioridad: Baja)
*Nota: Los pagos dependen totalmente de que ya existan citas agendadas o recetas emitidas.*
*   *Feature 5.1: Módulo de Pagos**
    *   Pago citas (Actividad 3)
    *   Pago medicamentos (Actividad 4)


# 3. Plan del Sprint 1

*   **Meta del Sprint:** Crear el núcleo de identidad del sistema (registros) y permitir la consulta de médicos disponibles.
*   *Entregable:** Código estructurado en GitHub que permita registrar Pacientes y Profesionales, e imprima en pantalla la lista de especialistas con sus horarios libres.

# Asignación de Tareas por Rol:

* Roles: Producto Owner: Juan Manuel Serna / Scrum Master: Angie Garcia / Dev Team: Lucas, Michael, Camilo

*   *Dev Team:**
    *   *Tarea 1:* Crear el repositorio, ejecutar comandos iniciales (`git init`, `git add .`, `git commit`) y desarrollar el registro de usuarios y profesionales.
    *   *Tarea 2:* Crear la base de datos lógica para almacenar y consultar la disponibilidad de los especialistas.
*   **Scrum Master:**
    *   *Tarea 3:* Controlar el flujo de Git en el equipo, resolver bloqueos de conexión y coordinar la simulación del Daily Scrum.
*   **Product Owner:Juan Manuel Serna**
    *   *Tarea 4:* Validar que los campos del registro de médicos coincidan con lo necesario para evaluar su disponibilidad en agenda.
