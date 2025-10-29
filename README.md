# HealthTrack
HealthTrack es una aplicación móvil desarrollada en Android Studio que permite a los usuarios registrar, visualizar y gestionar sus hábitos saludables diarios.
Nuestro objetivo principal es ofrecer una herramienta simple y funcional que fomente el autocuidado y la constancia en actividades como la alimentación, hidratación y ejercicio físico.

Funcionalidades principales

Interfaz visual organizada:
Pantalla de inicio con navegación hacia las secciones de registro de hábitos, historial de registros y perfil del usuario.
Diseño coherente y limpio, con una distribución clara de botones y campos.

Formularios validados:
Campos: tipo de hábito (agua, ejercicio, alimentación, etc.), descripción o cantidad y fecha.
Validaciones visuales con íconos e indicaciones.
Control lógico separado de la interfaz (patrón MVVM o controlador).

Lógica desacoplada:
Manejo de validaciones y estados desde el ViewModel o clases lógicas separadas.
Separación entre la capa visual y la lógica de negocio.

Animaciones funcionales:
Transiciones suaves entre pantallas.
Animaciones simples al registrar un nuevo hábito o visualizar el historial.

Estructura modular y persistencia:
Estructura del proyecto:


├── ui/           # Interfaces gráficas y pantallas

├── viewmodel/    # Lógica y control de estados

├── data/         # Persistencia con Room o SharedPreferences


Los datos se mantienen al cerrar y reabrir la aplicación.

Recursos nativos:

Cámara / galería: permite adjuntar una imagen del hábito (por ejemplo, una comida saludable).

GPS / localización: guarda la ubicación del registro automáticamente.
Uso responsable y seguro de los permisos del dispositivo.

Herramientas colaborativas:

Repositorio público en GitHub con commits descriptivos.

Gestión del proyecto en Trello, con planificación y tareas asignadas a cada integrante.

Integrantes y desarrolladores del proyecto:
David Coliqueo y Claudio Castillo.
