# HealthTrack - Aplicación de Seguimiento de Hábitos Saludables

## Descripción

HealthTrack es una aplicación Android moderna desarrollada con Kotlin y Jetpack Compose que permite a los usuarios registrar y monitorear sus hábitos saludables diarios, incluyendo:

- Consumo de agua: Registra cuánta agua bebes diariamente  
- Comidas: Registra tus comidas con fotos, calorías y ubicación  
- Ejercicio: Registra tus actividades físicas y calorías quemadas  
- Resumen visual: Visualiza tu progreso con estadísticas y gráficos  
- Historial: Consulta todos tus registros anteriores  

## Características Principales

### Formularios Validados
- Validación de campos requeridos  
- Tipos de entrada apropiados (números, texto)  
- Mensajes de error claros y útiles  

### Integración de Cámara
- Permite tomar fotos de las comidas directamente desde la aplicación  
- Las fotos se guardan localmente y se asocian con cada registro  

### Geolocalización
- Registra automáticamente la ubicación donde se consumen los alimentos  
- Muestra el nombre de la ubicación mediante geocodificación  
- Funciona con permisos de ubicación precisa y aproximada  

### Persistencia Local
- Base de datos Room para almacenamiento local  
- Los datos persisten entre sesiones  
- No requiere conexión a internet  

### Visualización de Datos
- Resumen diario con metas  
- Gráficos de progreso circulares  
- Balance calórico (calorías consumidas vs quemadas)  
- Indicadores visuales de cumplimiento de metas  

## Tecnologías Utilizadas

### Lenguaje y Framework
- Kotlin  
- Jetpack Compose  
- Material Design 3  

### Arquitectura
- MVVM (Model-View-ViewModel)  
- Repository Pattern  
- StateFlow para manejo reactivo del estado  

### Bibliotecas Principales
- Room (base de datos local SQLite)  
- Navigation Compose  
- Coil (carga y visualización de imágenes)  
- CameraX  
- Google Play Services Location  
- Accompanist Permissions  

## Estructura del Proyecto

com.example.healthtrack/
├── data/
│ ├── local/
│ │ ├── AppDatabase.kt
│ │ ├── Converters.kt
│ │ ├── WaterIntakeDao.kt
│ │ ├── MealRecordDao.kt
│ │ └── ExerciseDao.kt
│ ├── model/
│ │ ├── WaterIntake.kt
│ │ ├── MealRecord.kt
│ │ └── Exercise.kt
│ └── repository/
│ └── HealthRepository.kt
├── navigation/
│ ├── Screen.kt
│ └── AppNavigation.kt
├── ui/
│ ├── screens/
│ │ ├── HomeScreen.kt
│ │ ├── WaterIntakeScreen.kt
│ │ ├── MealRecordScreen.kt
│ │ ├── ExerciseScreen.kt
│ │ ├── HistoryScreen.kt
│ │ └── SummaryScreen.kt
│ ├── viewmodel/
│ │ ├── WaterIntakeViewModel.kt
│ │ ├── MealRecordViewModel.kt
│ │ ├── ExerciseViewModel.kt
│ │ └── SummaryViewModel.kt
│ └── theme/
│ ├── Color.kt
│ ├── Theme.kt
│ └── Type.kt
├── utils/
│ ├── CameraUtils.kt
│ ├── LocationHelper.kt
│ └── DateUtils.kt
└── MainActivity.kt

markdown
Copiar código

## Permisos Requeridos

- CAMERA: Para tomar fotos de las comidas  
- ACCESS_FINE_LOCATION: Para obtener la ubicación precisa  
- ACCESS_COARSE_LOCATION: Para obtener la ubicación aproximada  
- INTERNET: Para servicios de geocodificación  

## Pantallas de la Aplicación

### 1. Pantalla Principal (Home)
- Resumen del día actual  
- Accesos rápidos a cada funcionalidad  
- Estadísticas en tiempo real  

### 2. Registro de Agua
- Formulario para registrar la cantidad de agua  
- Visualización del total diario  
- Barra de progreso hacia la meta (2000 ml)  
- Historial de registros  

### 3. Registro de Comidas
- Selección del tipo de comida (Desayuno, Almuerzo, Cena, Snack)  
- Descripción de la comida  
- Calorías (opcional)  
- Foto de la comida (con cámara)  
- Ubicación automática  
- Notas adicionales  

### 4. Registro de Ejercicio
- Tipo de ejercicio  
- Duración en minutos  
- Calorías quemadas (opcional)  
- Notas adicionales  

### 5. Historial
- Vista unificada de todos los registros  
- Organizado por categorías  
- Opción para eliminar registros  

### 6. Resumen y Estadísticas
- Gráficos de progreso  
- Metas diarias con porcentajes  
- Balance calórico  
- Estadísticas generales  

## Configuración del Proyecto

### Requisitos Previos
- Android Studio Hedgehog o superior  
- Kotlin 2.0.21  
- SDK mínimo: Android 7.0 (API 24)  
- SDK objetivo: Android 15 (API 36)  

### Pasos para Ejecutar

1. Clonar o abrir el proyecto en Android Studio  
2. Sincronizar Gradle  
   - Android Studio sincronizará automáticamente las dependencias  
   - Si no lo hace, ejecutar: **Build > Sync Project with Gradle Files**  
3. Ejecutar la aplicación  
   - Conectar un dispositivo Android o iniciar un emulador  
   - Presionar **Run** o **Shift + F10**  

## Uso de la Aplicación

### Registrar Agua
1. Desde la pantalla principal, seleccionar "Agua"  
2. Presionar el botón flotante (+)  
3. Ingresar la cantidad en mililitros  
4. Añadir una nota opcional  
5. Presionar "Guardar"  

### Registrar Comida
1. Desde la pantalla principal, seleccionar "Comida"  
2. Presionar el botón flotante (+)  
3. Seleccionar el tipo de comida  
4. Ingresar la descripción  
5. Añadir calorías, foto o notas si se desea  
6. La ubicación se captura automáticamente si los permisos están otorgados  
7. Presionar "Guardar"  

### Registrar Ejercicio
1. Desde la pantalla principal, seleccionar "Ejercicio"  
2. Presionar el botón flotante (+)  
3. Ingresar el tipo de ejercicio  
4. Ingresar la duración  
5. Añadir calorías quemadas o notas si se desea  
6. Presionar "Guardar"  

### Ver Estadísticas
1. Desde la pantalla principal, seleccionar "Resumen"  
2. Visualizar las metas del día  
3. Revisar el balance calórico  
4. Presionar el botón de actualizar para refrescar los datos  

## Metas Predeterminadas

- Agua: 2000 ml por día  
- Calorías: 2000 kcal por día  
- Ejercicio: 30 minutos por día  

## Base de Datos

HealthTrack utiliza Room con las siguientes tablas:

### water_intake
- id (PK)  
- amountMl  
- timestamp  
- note  

### meal_records
- id (PK)  
- mealType  
- description  
- calories  
- photoUri  
- latitude  
- longitude  
- locationName  
- timestamp  
- notes  

### exercises
- id (PK)  
- exerciseType  
- durationMinutes  
- caloriesBurned  
- timestamp  
- notes  

## Solución de Problemas

### La cámara no funciona
- Verificar que los permisos de cámara estén otorgados  
- Revisar en Configuración del dispositivo > Aplicaciones > HealthTrack > Permisos  

### La ubicación no se captura
- Verificar los permisos de ubicación  
- Activar el GPS del dispositivo  
- Asegurarse de estar en un lugar con buena recepción  

### Los datos no se guardan
- Verificar que haya espacio suficiente en el dispositivo  
- Revisar los registros de Android Studio en caso de error  

## Licencia

Este proyecto fue desarrollado con fines educativos.

## Autor

Desarrollado utilizando Android Studio y Kotlin.

## Características Futuras Posibles

- Gráficos semanales y mensuales  
- Exportar datos a CSV  
- Recordatorios para beber agua  
- Widget de pantalla principal  
- Modo oscuro  
- Sincronización en la nube  
- Análisis nutricional avanzado  
- Integración con dispositivos portátiles  
- Compartir logros en redes sociales 
