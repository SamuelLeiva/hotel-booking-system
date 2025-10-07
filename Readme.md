# 🏨 Hotel Booking System (NestJS + Arquitectura Híbrida)

Un sistema de reservas de hotel escalable desarrollado con **NestJS**, siguiendo un enfoque **de microservicios híbrido** (bases de datos SQL + NoSQL) para manejar eficientemente tanto datos estructurados como no estructurados.

## 🚀 Objetivo del Proyecto

Diseñar y desarrollar un **sistema de reservas hoteleras moderno y eficiente**, capaz de manejar grandes volúmenes de tráfico, integrando servicios independientes y tecnologías mixtas de persistencia.

Este proyecto está enfocado en mostrar **arquitectura profesional**, **buenas prácticas de diseño** y **documentación clara**, ideal para presentar en un portafolio de GitHub técnico.

---

## 🧩 Arquitectura General

El sistema se compone de varios microservicios independientes comunicados a través de un **API Gateway**.  
Se emplea una **arquitectura híbrida**:

- **SQL (PostgreSQL/MySQL)** → Para datos estructurados (usuarios, reservas, pagos)
- **NoSQL (MongoDB)** → Para datos dinámicos o no estructurados (logs, notificaciones, historial de búsquedas)

### 🏗️ Microservicios Principales del MVP

1. **User Service**  
   - Gestiona usuarios, roles y autenticación.

2. **Room Service**  
   - Administra habitaciones, tipos, disponibilidad y características.

3. **Booking Service**  
   - Maneja las reservas, disponibilidad y relación entre usuarios y habitaciones.

4. **Payment Service**  
   - Procesa pagos y registra transacciones.

5. **Notification Service**  
   - Envía correos o notificaciones tras reservas o cancelaciones.

---

## 📚 Historias de Usuario — MVP

A continuación se presentan las **historias de usuario mínimas necesarias** para el primer incremento funcional del sistema (MVP), organizadas por microservicio.

---

### 👤 User Service

#### HU1: Registro de usuario
**Como** huésped  
**Quiero** registrarme con mis datos personales y credenciales  
**Para** poder acceder al sistema y realizar reservas.  

#### HU2: Inicio de sesión
**Como** usuario registrado  
**Quiero** iniciar sesión con mis credenciales  
**Para** acceder a mi perfil y gestionar mis reservas.

#### HU3: Visualizar perfil
**Como** usuario autenticado  
**Quiero** ver mi información personal  
**Para** asegurarme de que mis datos están correctos.

---

### 🏠 Room Service

#### HU4: Listar habitaciones disponibles
**Como** huésped  
**Quiero** ver todas las habitaciones disponibles  
**Para** elegir la que mejor se adapte a mis necesidades.

#### HU5: Ver detalles de una habitación
**Como** huésped  
**Quiero** ver los detalles de una habitación (precio, tipo, servicios incluidos, fotos)  
**Para** tomar una decisión informada antes de reservar.

---

### 📅 Booking Service

#### HU6: Crear una reserva
**Como** usuario autenticado  
**Quiero** realizar una reserva seleccionando habitación y fechas  
**Para** asegurar mi estadía.

#### HU7: Ver mis reservas activas
**Como** usuario autenticado  
**Quiero** consultar mis reservas actuales  
**Para** tener control sobre mis estancias futuras.

#### HU8: Cancelar una reserva
**Como** usuario autenticado  
**Quiero** cancelar una reserva antes de la fecha de inicio  
**Para** liberar la habitación y evitar cargos innecesarios.

---

### 💳 Payment Service

#### HU9: Procesar el pago de una reserva
**Como** usuario autenticado  
**Quiero** realizar el pago de mi reserva mediante tarjeta o medio digital  
**Para** confirmar mi reserva con éxito.

#### HU10: Ver historial de pagos
**Como** usuario autenticado  
**Quiero** ver mis pagos realizados  
**Para** tener un registro de mis transacciones.

---

### 📩 Notification Service

#### HU11: Notificación de confirmación
**Como** usuario  
**Quiero** recibir una notificación o correo electrónico de confirmación  
**Para** saber que mi reserva y pago fueron procesados correctamente.

#### HU12: Notificación de cancelación
**Como** usuario  
**Quiero** recibir un aviso al cancelar una reserva  
**Para** confirmar que la cancelación fue exitosa.

---

## ⚙️ Tecnologías Principales

| Componente              | Tecnología / Herramienta |
|--------------------------|---------------------------|
| Framework principal      | NestJS                    |
| Comunicación             | REST / gRPC (entre microservicios) |
| API Gateway              | Nginx / NestJS Gateway    |
| Base de datos relacional | PostgreSQL                |
| Base de datos NoSQL      | MongoDB                   |
| Autenticación            | JWT + Passport.js         |
| ORM                     | Prisma / TypeORM          |
| Mensajería interna       | RabbitMQ / Kafka (según implementación) |

---

## 🧠 Diseño del Sistema

El sistema sigue los principios de **Domain-Driven Design (DDD)** y **Clean Architecture**, dividiendo la lógica en capas bien definidas:

- `core/domain` → Entidades y lógica de negocio pura  
- `core/use-cases` → Casos de uso  
- `infrastructure` → Conexión con bases de datos, mensajería, APIs externas  
- `presentation` → Controladores y DTOs (NestJS)

---

## 🧩 Diagrama de Arquitectura Híbrida

*(Incluye el gráfico)*

---

## 📈 Próximos Pasos

- Implementar casos de uso secundarios: gestión de empleados, reportes, mantenimiento de habitaciones.  
- Añadir autenticación OAuth y administración de roles.  
- Integrar dashboard administrativo.  
- Implementar CI/CD y despliegue en Vercel o AWS.

---

## 🧑‍💻 Autor

**Samuel Leiva**  
Desarrollador Backend | Arquitectura Limpia | Node.js | NestJS  
[GitHub](https://github.com/) • [LinkedIn](https://linkedin.com/)

---