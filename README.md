HealthTrack

HealthTrack es una aplicación móvil desarrollada en Android Studio que permite a los usuarios registrar, visualizar y gestionar sus hábitos saludables diarios. Nuestro objetivo principal es ofrecer una herramienta simple y funcional que fomente el autocuidado y la constancia en actividades como la alimentación, hidratación y ejercicio físico.

Funcionalidades principales
Interfaz visual organizada

Pantalla de inicio con navegación hacia las secciones de registro de hábitos, historial de registros y perfil del usuario.

Diseño coherente y limpio, con una distribución clara de botones y campos.

Formularios validados

Campos para tipo de hábito (agua, ejercicio, alimentación, etc.), descripción o cantidad y fecha.

Validaciones visuales con íconos e indicaciones.

Control lógico separado de la interfaz (patrón MVVM o controlador).

Lógica desacoplada

Manejo de validaciones y estados desde el ViewModel o clases lógicas separadas.

Separación entre la capa visual y la lógica de negocio.

Animaciones funcionales

Transiciones suaves entre pantallas.

Animaciones simples al registrar un nuevo hábito o visualizar el historial.

Estructura modular y persistencia
├── ui/           # Interfaces gráficas y pantallas
├── viewmodel/    # Lógica y control de estados
├── data/         # Persistencia con Room o SharedPreferences


Los datos se mantienen al cerrar y reabrir la aplicación.

Recursos nativos
Cámara / galería

Permite adjuntar una imagen del hábito (por ejemplo, una comida saludable).

GPS / localización

Guarda la ubicación del registro automáticamente, utilizando una implementación segura del sistema de permisos del dispositivo.

✅ Integración de API externa: Consejos motivacionales

HealthTrack integra una API pública externa para mostrar consejos motivacionales de bienestar dentro de la aplicación. Esta funcionalidad ayuda a reforzar hábitos positivos con mensajes breves y directos.

API utilizada

Advice Slip API
URL base: https://api.adviceslip.com/advice
Proporciona frases motivacionales en inglés mediante solicitudes HTTP GET.

Tecnologías usadas

Retrofit 2.11.0 → Para realizar las solicitudes HTTP.

Gson Converter → Para parsear el JSON recibido desde la API.

Coroutines → Para manejar las llamadas de forma asíncrona.

ViewModel + StateFlow → Para exponer el estado a la UI de manera reactiva.

Dónde se integra en la app

El consejo se muestra en la pantalla de Resumen (SummaryScreen) a través de un componente llamado MotivationCard, que permite:

Ver un consejo motivacional actualizado.

Recargar un nuevo consejo con un botón “Otro consejo”.

Mostrar estado de carga o error si la API no responde.

Detalles de implementación

Archivo de cliente: MotivationRetrofitClient.kt

Servicio API: MotivationApiService.kt

Modelos: AdviceSlipResponse, AdviceSlip

ViewModel: MotivationViewModel

Ejemplo de respuesta de la API
{
  "slip": {
    "id": 180,
    "advice": "Keep going. Everything you need will come at the perfect time."
  }
}

Visualización

La aplicación muestra:

Un encabezado en español indicando que el contenido proviene de una API externa.

El consejo original en inglés (la API no soporta traducciones).

Botón para obtener un nuevo consejo.

Esto cumple con el requisito de la evaluación de incorporar y reflejar visualmente datos provenientes de una API externa real.

Herramientas colaborativas

Repositorio público en GitHub con commits descriptivos y participación de ambos integrantes.

Gestión del proyecto en Trello, con planificación y tareas asignadas a cada integrante.

Integrantes del proyecto

David Coliqueo

Claudio Castillo
