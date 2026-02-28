System Brief v1 — FastOrder
1) Nombre del sistema

FastOrder — Sistema de Gestión de Pedidos con Prioridad y Tiempo Estimado de Entrega

2) Problema que resuelve

Muchos negocios gestionan pedidos mediante llamadas telefónicas o mensajes, lo que provoca desorganización y retrasos en las entregas.
No existe un control claro sobre qué pedidos deben entregarse primero ni cuánto tiempo tomará cada entrega.
Esto genera errores, pérdida de tiempo y clientes insatisfechos.
El sistema FastOrder digitaliza la toma de pedidos permitiendo asignar prioridades automáticamente y calcular tiempos estimados según distancia.
Además, facilita la organización del trabajo de los repartidores y mejora la eficiencia del servicio de entrega.
El objetivo es optimizar el proceso de pedidos y garantizar entregas rápidas y ordenadas.

3) Usuarios / Stakeholders

Cliente

Operador de pedidos

Repartidor

Administrador del sistema

Dueño del negocio

4) Objetivos de éxito

Reducir el tiempo de registro de pedidos a menos de 2 minutos.

Mostrar tiempo estimado de entrega en todos los pedidos.

Disminuir retrasos de entrega en un 30%.

Mejorar la organización de pedidos urgentes.

5) Alcance (Incluye)

Registro de clientes.

Creación y administración de pedidos.

Clasificación automática por prioridad.

Cálculo de tiempo estimado de entrega.

Asignación de pedidos a repartidores.

Actualización del estado del pedido.

Notificaciones al cliente.

6) Fuera de alcance (No incluye)

Facturación electrónica.

Pagos en línea.

Integración avanzada con GPS.

Control completo de inventario.

7) Supuestos

Los clientes proporcionan direcciones correctas.

El negocio cuenta con repartidores disponibles.

El sistema funcionará con conexión a internet.

El cálculo inicial del tiempo se basa en distancia promedio.

8) Riesgos y mitigaciones

Riesgo: Direcciones incorrectas.
Mitigación: Validación obligatoria antes de confirmar pedido.

Riesgo: Exceso de pedidos en horas pico.
Mitigación: Sistema de prioridad automática.

Riesgo: Retrasos por tráfico o distancia.
Mitigación: Ajuste dinámico del tiempo estimado.

9) Requerimientos v1
Funcionales (FR)

FR-01: Registrar clientes y direcciones.

FR-02: Crear pedidos.

FR-03: Asignar prioridad automática al pedido.

FR-04: Calcular tiempo estimado de entrega.

FR-05: Asignar pedidos a repartidores.

FR-06: Actualizar estado del pedido.

FR-07: Consultar estado del pedido.

FR-08: Enviar notificaciones al cliente.

No Funcionales (NFR)

NFR-01: Tiempo de respuesta menor a 3 segundos.

NFR-02: Disponibilidad del sistema ≥ 99%.

NFR-03: Acceso seguro mediante autenticación.

NFR-04: Interfaz usable para crear pedidos en ≤ 2 min

10) Diagrama de Contexto (Mermaid)
    ```mermaid
flowchart LR
  Cliente -->|Realiza pedido| FastOrder
  Operador -->|Gestiona pedidos| FastOrder
  Repartidor -->|Entrega pedido| FastOrder
  Administrador -->|Configura| FastOrder

  FastOrder --> DB[(Base de Datos)]
  FastOrder --> Notificaciones[Servicio de Notificaciones]
