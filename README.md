IPOO Check-in — Sistema de Boletería y Reserva de Asientos

Aplicación de escritorio en Java Swing para la gestión de reservas, consulta de pasajes y selección visual de asientos en un vuelo.

Proyecto desarrollado bajo el paradigma de Programación Orientada a Objetos (POO). Permite simular el proceso de check-in y administración de butacas de una aeronave mediante una interfaz gráfica interactiva superpuesta sobre el plano de un avión.


Funcionalidades principales

* Mapa Interactivo de Asientos: Grilla visual de 15 filas × 5 columnas (con pasillo central diferenciado) que muestra en tiempo real qué butacas están disponibles, ocupadas o seleccionadas.
* Reserva de Pasajes: Validación de DNI numérico, verificación de duplicados (un pasajero por DNI), registro de nombre y apellido, y selección gráfica de ubicación 
* Generación Automática de Ticket: Creación de un código único de reserva formado por las iniciales del pasajero seguidas de su DNI (ej. `JP12345678`).
* Consulta de Reservas: Búsqueda rápida por DNI para visualizar los datos del pasajero, su ubicación asignada y el código de ticket.
* Cancelación y Liberación: Posibilidad de eliminar una reserva existente, liberando automáticamente el asiento en el mapa de la aeronave.

---

Tecnologías y conceptos aplicados

* Lenguaje: Java (JDK 8+)
* Interfaz Gráfica: Java Swing & AWT (`JFrame`, `JLayeredPane`, `GridLayout`, `BorderLayout`, manejo de eventos con `ActionListener` y recursos gráficos).
* Arquitectura y Diseño:** Separación entre lógica de negocio (`Logica`, `Vuelo`, `Reserva`) e interfaz de usuario (`GUI`, `MiBoton`), uso de matrices bidimensionales para el mapeo de asientos.

---

Estructura del proyecto

```text
├── Principal.java           # Punto de entrada de la aplicación (método main)
├── GUI.java                 # Interfaz gráfica principal, paneles y oyentes de eventos
├── MiBoton.java             # Componente personalizado (JButton) para botones y butacas
├── Logica.java              # Controlador principal que instancia y gestiona el vuelo
├── Vuelo.java               # Modelo del avión (matriz de reservas y operaciones de búsqueda/cancelación)
├── Reserva.java             # Modelo de datos del pasajero y su ticket asignado
├── avion_fondo.jpg          # Imagen de fondo de la cabina/aeronave
├── asiento.png              # Ícono de asiento disponible
└── asientoSeleccionado.png  # Ícono de asiento seleccionado actualmente

