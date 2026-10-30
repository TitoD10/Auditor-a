# Auditor-a
Aplicación web diseñada para la creación, registro y gestión de auditorías (para escuelas, construcciones, empresas, etc.). Su objetivo principal es prevenir fallas operativas y económicas mediante un sistema de alertas en tiempo real con notificaciones dictadas por voz para los administradores.

Objetivos

Objetivo General:
Desarrollar una aplicación web práctica y funcional para la gestión de auditorías que notifique a los administradores sobre fallas mediante un sistema de alertas con lectura de voz.

Objetivos Específicos:
Implementar un sistema de autenticación básico con dos roles: Auditor y Administrador.
Diseñar un formulario estándar para el registro y envío de datos de auditoría.
Desarrollar un panel de control para el administrador donde se reciban las notificaciones.
Integrar síntesis de voz en el navegador para dictar el contenido de las alertas recibidas.
Crear una vista de historial para consultar auditorías pasadas

Alcance y Limitaciones
Alcance:
El proyecto cubrirá el flujo completo y esencial de una auditoría: registro de usuario, llenado del formulario de inspección, envío de datos a la base de datos, y la visualización/reproducción por voz de la alerta en el panel del administrador. Se enfocará en un diseño modular y directo para mantener el desarrollo ágil.

Limitaciones:

No incluirá modo fuera de línea (offline); requiere conexión a internet para guardar los datos.

Las notificaciones se verán al recargar el panel de control o mediante peticiones simples, sin implementar infraestructuras complejas de WebSockets en tiempo real.

Los formularios de auditoría tendrán una estructura general estandarizada en lugar de un creador de formularios dinámico complejo.

Requerimientos Funcionales

Autenticación: El sistema debe permitir el registro e inicio de sesión de usuarios y administradores de empresas.

Registro de Auditorías: Los usuarios deben poder rellenar y enviar un formulario con los detalles y observaciones de la auditoría.

Gestión de Alertas: El sistema debe generar una alerta en el panel del administrador correspondiente al recibir un nuevo formulario.

Reproducción por Voz: El sistema debe incluir un botón de "Escuchar" en la notificación que dicte el contenido del reporte o que dicte el contenido del reporte de forma automática.

Historial: El sistema debe listar el registro de auditorías previas para su consulta.

Requerimientos No Funcionales

Usabilidad: Interfaz limpia, intuitiva y adaptable a dispositivos móviles (Responsive Design).

Eficiencia: El dictado de voz debe procesarse localmente en el navegador del administrador para no consumir almacenamiento ni ancho de banda del servidor.

Seguridad: Las contraseñas de los usuarios deben almacenarse de forma encriptada en la base de datos.

Disponibilidad: La base de datos debe estar alojada en la nube para garantizar el acceso a la información desde cualquier equipo.

Arquitectura de Desarrollo

Patrón: Arquitectura Cliente-Servidor simplificada (Frontend separado del Backend).

Lógica de Renderizado: El servidor actuará únicamente como una API (JSON) para recibir y enviar los datos, mientras que el cliente se encargará de construir la interfaz.

Stack Tecnológico

Frontend (Interfaz y Lógica de Cliente): HTML, CSS y TypeScript.

Motor de Voz: Web Speech API nativa de los navegadores web (sin librerías externas de audio).

Backend (Servidor): Node.js.
Base de Datos: PostgreSQL alojada en la nube (utilizando servicios como Neon para un despliegue rápido y gratuito).
