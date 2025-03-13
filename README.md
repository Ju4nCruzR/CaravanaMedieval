# CaravanaMedieval
Juego de estrategia y comercio medieval en Java Spring Boot - Proyecto Desarrollo Web

![image](https://github.com/user-attachments/assets/5d060bda-2dbe-41ff-9c08-a6213ae8cca5)

# Casos de uso
# Registrar una caravana
Actor: Jugador
Descripción: Un jugador crea una nueva caravana con atributos específicos.Flujo principal:

1. El jugador accede a la opción de "Registrar Caravana".
2. Ingresa los datos de la caravana: nombre, velocidad, capacidad de carga, dinero inicial y puntos de vida.
3. El sistema valida los datos ingresados.
4. Si los datos son correctos, la caravana es registrada en la base de datos.
5. El sistema confirma el registro exitoso.

Excepciones:
- Si algún dato es inválido (por ejemplo, velocidad negativa), el sistema muestra un mensaje de error y solicita corrección.

# Agregar un jugador a una Caravana
Actor: Administrador del juego
Descripción: Se asigna un jugador a una caravana existente.Flujo principal:

1. El administrador selecciona una caravana disponible.
2. Ingresa el nombre y rol del nuevo jugador.
3. El sistema valida que la caravana existe.
4. Se asigna el jugador a la caravana y se guarda en la base de datos.
5. El sistema muestra un mensaje de confirmación.

Excepciones:
- Si la caravana no existe, el sistema muestra un mensaje de error.
- Si el jugador ya pertenece a otra caravana, el sistema evita la asignación.

# Comprar Producto en una Ciudad
Actor: Jugador
Descripción: Un jugador compra un producto en la ciudad actual de su caravana.Flujo principal:

1. El jugador selecciona la opción "Comprar Producto".
2. Se muestran los productos disponibles en la ciudad.
3. El jugador elige un producto y la cantidad a comprar.
4. El sistema verifica si la caravana tiene suficiente dinero y capacidad de carga.
5. Si es posible, se descuenta el dinero y se agrega el producto al inventario de la caravana.
6. El sistema confirma la compra.

Excepciones:
- Si la caravana no tiene suficiente dinero, la compra es rechazada.
- Si la capacidad de carga se excede, el sistema muestra un error.

# Viajar a otra Ciudad
Actor: Jugador
Descripción: La caravana se desplaza a otra ciudad utilizando una ruta.Flujo principal:

1. El jugador selecciona la opción "Viajar".
2. Se muestran las rutas disponibles desde la ciudad actual.
3. El jugador elige una ruta.
4. El sistema verifica si la ruta es segura o peligrosa.
5. Si es segura, la caravana llega a la ciudad destino sin problemas.
6. Si es peligrosa, se aplica el daño correspondiente a la caravana.
7. Se actualiza la posición de la caravana en la base de datos.
8. Se muestra un mensaje de éxito.

Excepciones:
- Si la caravana no tiene dinero suficiente para los impuestos de entrada, no puede viajar.
- Si la caravana es destruida por el daño de la ruta, se notifica al jugador.

# Usar un Servicio en una Ciudad
Actor: Jugador
Descripción: Un jugador accede a un servicio en la ciudad donde está su caravana.Flujo principal:

1. El jugador selecciona la opción "Usar Servicio".
2. Se muestran los servicios disponibles en la ciudad.
3. El jugador elige un servicio (ejemplo: "Reparar caravana").
4. El sistema verifica si la caravana tiene suficiente dinero.
5. Si es posible, se realiza el servicio y se descuenta el costo.
6. Se actualiza la información de la caravana (ejemplo: reparación de puntos de vida).
7. Se muestra una confirmación.

Excepciones:
- Si la caravana no tiene suficiente dinero, el servicio no puede realizarse.

# Diagrama de Clases
![Diagrama de Clases CaravanaMedieval](https://github.com/user-attachments/assets/a2d07cdf-dca6-4b28-9dd8-7a007c1dbf11)

