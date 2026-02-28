# FastOrder 
Sistema de Gestión de Pedidos con Prioridad y Tiempo Estimado de Entrega

---

## 1️ Nombre del sistema
**FastOrder — Sistema de Gestión Inteligente de Pedidos**

---

## 2️ Problema que resuelve
Muchos negocios gestionan pedidos mediante llamadas o mensajes, causando desorganización y retrasos en las entregas.  
No existe control sobre qué pedidos deben atenderse primero ni cuánto tiempo tomará la entrega.  
Esto provoca errores, pérdida de tiempo y clientes insatisfechos.  
FastOrder permite registrar pedidos digitalmente, asignar prioridad automática y calcular tiempos estimados según distancia.  
El sistema mejora la organización del trabajo y optimiza el proceso de entrega.

---

## 3️ Usuarios / Stakeholders
- Cliente
- Operador de pedidos
- Repartidor
- Administrador del sistema
- Dueño del negocio

---

## 4️ Objetivos de éxito
- Reducir el tiempo de registro de pedidos a menos de 2 minutos.
- Mostrar tiempo estimado de entrega en todos los pedidos.
- Disminuir retrasos de entrega en un 30%.
- Mejorar la organización de pedidos prioritarios.

---

## 5️ Alcance (Incluye)
- Registro de clientes.
- Creación de pedidos.
- Clasificación automática por prioridad.
- Cálculo del tiempo estimado de entrega.
- Asignación de pedidos a repartidores.
- Actualización del estado del pedido.
- Envío de notificaciones al cliente.

---

## 6️ Fuera de alcance (No incluye)
- Facturación electrónica.
- Pagos en línea.
- Integración GPS avanzada.
- Control completo de inventario.

---

## 7️ Supuestos
- Los clientes proporcionan direcciones correctas.
- El negocio cuenta con repartidores disponibles.
- El sistema funcionará con conexión a internet.
- El tiempo estimado se basa en distancia promedio.

---

## 8️ Riesgos y mitigaciones

**Riesgo:** Direcciones incorrectas.  
**Mitigación:** Validación obligatoria antes de confirmar pedido.

**Riesgo:** Exceso de pedidos en horas pico.  
**Mitigación:** Priorización automática.

**Riesgo:** Retrasos por tráfico o distancia.  
**Mitigación:** Ajuste dinámico del tiempo estimado.

---

## 9️ Requerimientos v1

### Funcionales (FR)
- FR-01: Registrar clientes y direcciones.
- FR-02: Crear pedidos.
- FR-03: Asignar prioridad automática.
- FR-04: Calcular tiempo estimado de entrega.
- FR-05: Asignar pedidos a repartidores.
- FR-06: Actualizar estado del pedido.
- FR-07: Consultar estado del pedido.
- FR-08: Enviar notificaciones al cliente.

### No Funcionales (NFR)
- NFR-01: Tiempo de respuesta menor a 3 segundos.
- NFR-02: Disponibilidad del sistema ≥ 99%.
- NFR-03: Acceso seguro mediante autenticación.
- NFR-04: Interfaz usable para crear pedidos en ≤ 2 minutos.

---

## 10 Diagrama de Contexto

```mermaid
flowchart LR
  Cliente -->|Realiza pedido| FastOrder
  Operador -->|Gestiona pedidos| FastOrder
  Repartidor -->|Entrega pedido| FastOrder
  Administrador -->|Configura| FastOrder

  FastOrder --> DB[(Base de Datos)]
  FastOrder --> Notificaciones[Servicio de Notificaciones]
