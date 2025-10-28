# HealthTrack
Integrantes y Desarrolladores del proyecto: David Coliqueo, Claudio Castillo
HealthTrack es una aplicacion movil desarrollada en Android Studio la cual permite a los usuarios, registrar, visualizar y gestionar sus habitos saludables diarios. nuestro objetivo principal es ofrecer una herramienta simple y funcional que ayude a fomentar el autocuidado y la constancia en actividades como la alimentacion, hidratacion y ejercicio fisico 

Funcionalidades Principales:

1. Interfaz visual organizada con pantalla de inicio con navegación hacia: Registro de hábitos, Historial de registros, Perfil del usuario, Diseño coherente y limpio, con distribución clara de botones y campos.
2. Formularios validados: Campos: Tipo de hábito (Agua, Ejercicio, Alimentación, etc.), Descripción o cantidad, Fecha, Validaciones visuales con íconos e indicaciones. Control lógico separado de la interfaz (MVVM o Controlador).
3. Lógica desacoplada Manejo de validaciones y estados desde ViewModel o clases lógicas separadas.Separación entre capa visual y lógica de negocio.
4. Animaciones funcionales Transiciones suaves entre pantallas. Animación simple al registrar un nuevo hábito o visualizar el historial.
5. Estructura modular y persistencia
Estructura del proyecto:
├── ui/           # Interfaces gráficas y pantallas
├── viewmodel/    # Lógica y control de estados
├── data/         # Persistencia con Room o SharedPreferences
Los datos se mantienen al cerrar y reabrir la aplicación.
6. Recursos nativos Cámara / Galería: permite adjuntar una imagen del hábito (por ejemplo, comida saludable).GPS / Localización: guarda la ubicación del registro automáticamente.Uso responsable y seguro de permisos.
7. Herramientas colaborativas Repositorio público en GitHub con commits descriptivos. Archivo README.md (este documento). Gestión en Trello, con planificación y tareas asignadas por integrante.
