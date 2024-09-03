# Historias de Usuario

## Historia de Usuario 1: Registro de Usuario

**Como** usuario de la aplicación  
**Quiero** registrarme con mi cuenta de Gmail  
**Para** poder acceder a la aplicación y realizar compras

### Criterios de Aceptación
- El usuario debe poder ingresar su dirección de correo electrónico de Gmail.
- El sistema debe validar que el correo electrónico sea válido y esté registrado en Gmail.
- Tras el registro exitoso, el usuario debe recibir un mensaje de confirmación.

### Supuestos
- La aplicación tiene acceso a la API de Gmail para validar las direcciones de correo electrónico.
- El sistema de registro está integrado con el backend para manejar los datos de usuario.

---

## Historia de Usuario 2: Ingreso de Datos del Vehículo

**Como** usuario que realiza una compra  
**Quiero** ingresar los datos del vehículo para calcular el costo de despacho  
**Para** recibir una estimación precisa del costo de envío basado en la distancia

### Criterios de Aceptación
- El usuario debe poder ingresar los siguientes datos: Marca, Modelo, Cilindrada, Tipo de Combustible y Capacidad en pasajeros.
- El sistema debe mostrar un resumen de los datos ingresados.
- El sistema debe calcular y mostrar el costo del despacho basado en las reglas de negocio.

### Supuestos
- Los datos ingresados por el usuario se almacenan correctamente en la base de datos.
- El cálculo del costo de despacho se realiza en base a las reglas predefinidas.

---

## Historia de Usuario 3: Cálculo de Costo de Despacho

**Como** usuario que ha ingresado los datos del vehículo  
**Quiero** que el sistema calcule el costo del despacho  
**Para** saber cuánto pagaré por el envío antes de finalizar mi compra

### Criterios de Aceptación
- El sistema debe calcular el costo de despacho en función de la compra total y la distancia.
  - Compras mayores a 50,000 pesos deben ser enviadas gratis.
  - Compras entre 25,000 y 49,999 pesos deben pagar $150 por kilómetro.
  - Compras menores a 25,000 pesos deben pagar $300 por kilómetro.
- El costo del despacho calculado debe mostrarse claramente al usuario antes de la confirmación de la compra.

### Supuestos
- El sistema tiene acceso a la distancia entre el usuario y la ubicación de despacho.
- Las tarifas de despacho están correctamente configuradas en el sistema.

---

## Historia de Usuario 4: Confirmación de Compra

**Como** usuario que ha revisado el costo de despacho  
**Quiero** confirmar mi compra  
**Para** completar el proceso de compra y recibir el producto

### Criterios de Aceptación
- El usuario debe poder revisar el resumen de la compra y el costo de despacho.
- El sistema debe permitir al usuario confirmar la compra y generar un recibo.
- El usuario debe recibir un mensaje de confirmación y detalles de la compra por correo electrónico.

### Supuestos
- El sistema de pagos está integrado y funcional.
- El sistema envía correos electrónicos de confirmación correctamente.

---

## Historia de Usuario 5: Acceso a Historial de Compras

**Como** usuario registrado  
**Quiero** acceder a mi historial de compras  
**Para** revisar mis compras anteriores y verificar detalles

### Criterios de Aceptación
- El usuario debe poder acceder a un historial de compras desde su perfil.
- El historial debe mostrar detalles como fecha de compra, productos adquiridos, y costo de despacho.
- El usuario debe poder buscar y filtrar el historial de compras.

### Supuestos
- Los datos de compras se almacenan correctamente en la base de datos.
- La interfaz de usuario permite la visualización y filtrado del historial de compras.

