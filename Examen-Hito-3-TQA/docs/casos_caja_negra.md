# Casos de caja negra — resultados reales

## TC-001: Inicio de sesión exitoso
- **Estado:** PASSED
- **Precondiciones:** Sesión cerrada y página de acceso visible.
- **Datos:** Usuario: standard_user; contraseña: secret_sauce.
- **Pasos:** 1. Abrir SauceDemo. 2. Ingresar las credenciales. 3. Pulsar Login.
- **Esperado:** Se muestra el catálogo y la URL inventory.html.
- **Observado:** El catálogo de seis productos quedó visible en inventory.html.
- **Evidencia:** `evidencias/capturas/TC001_catalogo.png`

## TC-002: Agregar un producto al carrito
- **Estado:** PASSED
- **Precondiciones:** Sesión iniciada; carrito inicialmente vacío.
- **Datos:** Producto: Sauce Labs Backpack; precio: $29.99; cantidad: 1.
- **Pasos:** 1. Localizar Sauce Labs Backpack. 2. Pulsar Add to cart. 3. Revisar el contador del carrito.
- **Esperado:** El botón cambia a Remove y el contador muestra 1.
- **Observado:** El botón cambió a Remove y el indicador del carrito mostró 1.
- **Evidencia:** `evidencias/capturas/TC002_agregar.png`

## TC-003: Eliminar un producto del carrito
- **Estado:** PASSED
- **Precondiciones:** La mochila está agregada al carrito.
- **Datos:** Sauce Labs Backpack; cantidad inicial: 1.
- **Pasos:** 1. Abrir el carrito. 2. Confirmar mochila y cantidad 1. 3. Pulsar Remove.
- **Esperado:** La mochila desaparece y el contador deja de mostrar 1.
- **Observado:** La mochila dejó de aparecer en el carrito y desapareció la insignia numérica.
- **Evidencia:** `evidencias/capturas/TC003_despues.png`

## TC-004: Completar una compra
- **Estado:** PASSED
- **Precondiciones:** Sesión iniciada, carrito con una luz para bicicleta.
- **Datos:** Sauce Labs Bike Light ($9.99); Ana; Perez; 12345.
- **Pasos:** 1. Abrir carrito. 2. Pulsar Checkout. 3. Completar tres campos. 4. Pulsar Continue. 5. Revisar resumen. 6. Pulsar Finish.
- **Esperado:** Se muestra resumen coherente y confirmación Thank you for your order!
- **Observado:** Se mostró subtotal $9.99, impuesto $0.80, total $10.79 y confirmación de pedido.
- **Evidencia:** `evidencias/capturas/TC004_confirmacion.png`

## TC-005: Validar código postal obligatorio
- **Estado:** PASSED
- **Precondiciones:** Sesión iniciada, producto en carrito y formulario Checkout: Your Information abierto.
- **Datos:** Nombre: Ana; apellido: Perez; código postal: vacío.
- **Pasos:** 1. Completar Ana y Perez. 2. Dejar Zip/Postal Code vacío. 3. Pulsar Continue.
- **Esperado:** La compra no avanza y se informa que falta el código postal.
- **Observado:** Se mantuvo el formulario y apareció Error: Postal Code is required.
- **Evidencia:** `evidencias/capturas/TC005_validacion.png`

