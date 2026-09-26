# Historias de Usuario Detalladas - SALUD_360

## Épica 1: Control de Accesos y Usuarios (Prioridad Alta) []
> **Justificación:** Es la base de la seguridad y personalización del sistema. Se deben identificar los ingresos de pacientes y profesionales antes de permitir el acceso a agendas médicas o datos de salud protegidos.

### Feature 1.1: Registro y Onboarding de Usuarios []
#### 📗 Historia de Usuario (Actividad 6): Registro de Pacientes []
* **Formato:** Como Paciente nuevo, quiero crear una cuenta con mis datos básicos para acceder a los servicios de la aplicación.
* **Criterios de Aceptación (CA):**
  * Validar campos obligatorios (cédula, nombre, correo, contraseña).
  * Enviar correo de confirmación.

#### 📗 Historia de Usuario (Actividad 7): Registro de Profesionales []
* **Formato:** Como Médico especialista, quiero registrar mi perfil junto a mi tarjeta profesional para ser habilitado en la agenda de la clínica.
* **Criterios de Aceptación (CA):**
  * Permitir adjuntar número de licencia médica.
  * Dejar el perfil en estado "Pendiente de aprobación" por el administrador.

### Feature 1.2: Autenticación y Sesiones Seguras []
#### 📗 Historia de Usuario (Actividad 8): Inicio de Sesión []
* **Formato:** Como Usuario registrado, quiero ingresar con mi correo y contraseña para acceder a mi panel personal confidencial.
* **Criterios de Aceptación (CA):**
  * Bloquear la cuenta tras 3 intentos fallidos.
  * Permitir recordar contraseña.

#### 📗 Historia de Usuario (Actividad 9): Cierre de Sesión []
* **Formato:** Como Usuario autenticado, quiero cerrar mi sesión de forma explícita para garantizar que nadie más vea mis datos de salud en este dispositivo.
* **Criterios de Aceptación (CA):**
  * Destruir los tokens de acceso activos y redirigir inmediatamente a la pantalla de Login.

---

## Épica 2: Agendar y Gestionar Citas (Prioridad Alta) []
> **Justificación:** Es el motor operativo diario de la clínica, nos permite coordinar la disponibilidad de los médicos con la cantidad de los pacientes para dar una buena atención.

### Feature 2.1: Motor de Búsqueda y Disponibilidad []
#### 📗 Historia de Usuario (Actividad 10): Consulta de Disponibilidad []
* **Formato:** Como Paciente, quiero filtrar los médicos por especialidad y fecha para encontrar un horario conveniente para mi atención.
* **Criterios de Aceptación (CA):**
  * Mostrar un calendario interactivo en tiempo real con horas libres por especialista.

### Feature 2.2: Gestión del Flujo de Citas []
#### 📗 Historia de Usuario (Actividad 1): Agendamiento de Citas []
* **Formato:** Como Paciente, quiero reservar un espacio médico seleccionado para asegurar mi consulta con el especialista.
* **Criterios de Aceptación (CA):**
  * Confirmar la reserva visualmente.
  * Enviar un correo con el resumen de la cita.

#### 📗 Historia de Usuario (Actividad 2): Modificación de Estado de Citas []
* **Formato:** Como Paciente/Administrador, quiero cancelar o reagendar una cita existente para liberar el espacio en la agenda si no puedo asistir.
* **Criterios de Aceptación (CA):**
  * Permitir cambios con un mínimo de 24 horas de anticipación.
  * Notificar automáticamente al médico asignado.

---

## Épica 3: Atención Clínica en Consulta (Prioridad Media)
> **Justificación:** Aquí se recopila el estado de los pacientes para tomar decisiones.

### Feature 3.1: Registro Clínico en Consulta (Módulo Médico)
#### 📗 Historia de Usuario (Actividad 12): Registrar Consulta Médica
* **Formato:** Como Médico, quiero escribir el motivo de consulta y el diagnóstico durante la cita para guardar el registro formal de la atención.
* **Criterios de Aceptación (CA):**
  * Incluir un buscador integrado de códigos diagnósticos CIE-10/CIE-11.

#### 📗 Historia de Usuario (Actividad 13): Registrar Signos Vitales
* **Formato:** Como Personal de enfermería, quiero ingresar la presión, temperatura y peso del paciente para completar el triaje previo a la consulta.
* **Criterios de Aceptación (CA):**
  * Marcar con alertas visuales (rojo/amarillo) si los signos están fuera de los rangos normales.

---

## Épica 4: Tratamientos, Medicamentos y Resultados (Prioridad Media)
> **Justificación:** Maneja el inventario de medicamentos, las fórmulas dadas por el médico y la entrega de diagnósticos. El equipo decidió mover la Historia Clínica aquí porque es un historial médico que se alimenta de las consultas y tratamientos aplicados.

### Feature 4.1: Expediente Clínico e Historial
#### 📗 Historia de Usuario (Actividad 5): Consultar Historias Clínicas
* **Formato:** Como Médico, quiero revisar las consultas y antecedentes previos del paciente para dar un diagnóstico preciso basado en su evolución.
* **Criterios de Aceptación (CA):**
  * Desplegar la información en orden cronológico descendente.
  * Acceso restringido según el rol del usuario.

#### 📗 Historia de Usuario (Actividad 11): Descarga de Resultados
* **Formato:** Como Paciente, quiero visualizar y descargar mis exámenes de laboratorio para compartirlos o guardarlos en mi dispositivo.
* **Criterios de Aceptación (CA):**
  * Habilitar la descarga directa en formato PDF.

### Feature 4.2: Gestión de Prescripciones y Stock
#### 📗 Historia de Usuario (Actividad 14): Registro de Tratamiento Médico
* **Formato:** Como Médico, quiero generar una receta digital con dosis y frecuencias para que el paciente sepa cómo tomar sus medicamentos.
* **Criterios de Aceptación (CA):**
  * Vincular la receta al historial del paciente de forma automática.

#### 📗 Historia de Usuario (Actividad 15): Catálogo e Inventario de Farmacia
* **Formato:** Como Farmacéutico, quiero ver el stock disponible de medicamentos para controlar los despachos y evitar desabastecimientos.
* **Criterios de Aceptación (CA):**
  * Restar del inventario automáticamente cada vez que se registre la entrega de una receta pagada.

---

## Épica 5: Transacciones y Facturación (Prioridad Baja)
> **Justificación:** Los pagos dependen de que existan citas agendadas y medicamentos formulados.

### Feature 5.1: Módulo de Pagos Integrado
#### 📗 Historia de Usuario (Actividad 3): Pago de Citas
* **Formato:** Como Paciente, quiero pagar el valor de mi consulta mediante PSE o tarjeta de crédito para confirmar la cita sin hacer filas en la clínica.
* **Criterios de Aceptación (CA):**
  * Conectar con pasarela segura.
  * Generar comprobante digital y enviarlo por correo.

#### 📗 Historia de Usuario (Actividad 4): Pago de Medicamentos
* **Formato:** Como Paciente, quiero pagar las medicinas de mi receta médica a través de la app para solicitar el envío a domicilio o el retiro express.
* **Criterios de Aceptación (CA):**
  * Aplicar descuentos o copagos si el usuario cuenta con seguro médico compatible.
