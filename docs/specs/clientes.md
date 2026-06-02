# Especificación: Gestión de Clientes

## Objetivo

Permitir registrar, consultar, modificar y eliminar clientes de la librería para asociarlos a las ventas realizadas.

---

## Descripción

La entidad Cliente representa a una persona que realiza compras en la librería.

---

## Propiedades

| Campo | Tipo | Obligatorio |
|---------|---------|---------|
| Cedula | string | Sí |
| Nombre | string | Sí |
| Apellido | string | Sí |
| Telefono | string | Sí |
| Correo | string | No |
| Direccion | string | No |

---

## Reglas de Negocio

RN01: La cédula debe ser única.

RN02: No se puede registrar un cliente sin nombre.

RN03: No se puede registrar un cliente sin apellido.

RN04: El teléfono debe contener únicamente números.

RN05: El correo electrónico debe tener un formato válido.

RN06: No se puede eliminar un cliente que tenga ventas registradas.

---

## Requisitos Funcionales

### RF01 - Registrar Cliente

El sistema debe permitir registrar un nuevo cliente.

#### Datos requeridos

- Cedula
- Nombre
- Apellido
- Telefono
- Correo
- Direccion

#### Criterios de aceptación

- La cédula no debe existir previamente.
- Todos los campos obligatorios deben estar completos.
- El cliente debe almacenarse correctamente.

---

### RF02 - Buscar Cliente

El sistema debe permitir buscar clientes por:

- Cédula
- Nombre

#### Criterios de aceptación

- Debe mostrar la información completa del cliente encontrado.

---

### RF03 - Modificar Cliente

El sistema debe permitir actualizar la información de un cliente existente.

#### Criterios de aceptación

- Debe validar las reglas de negocio.
- Debe actualizar la información correctamente.

---

### RF04 - Eliminar Cliente

El sistema debe permitir eliminar un cliente.

#### Criterios de aceptación

- Verificar que el cliente exista.
- Verificar que no tenga ventas asociadas.

---

### RF05 - Listar Clientes

El sistema debe mostrar todos los clientes registrados.

#### Información mostrada

- Cédula
- Nombre completo
- Teléfono
- Correo
