# Diagrama ER Normalizado

## Descripción general

El modelo representa la gestión de un taller, separando dos procesos principales:
- Operación (clientes y trabajos)
- Abastecimiento (materiales y pedidos)

## Entidades principales

### Cliente
Almacena la información de los clientes.

### Trabajo
Representa los trabajos solicitados por los clientes.

### Material
Contiene los materiales utilizados en los trabajos y adquiridos por el taller.

### Distribuidor
Proveedores de materiales.

### Pedido
Registro de compras realizadas a distribuidores.

---

## Relaciones importantes

### Material_Trabajo
Tabla intermedia que resuelve la relación muchos a muchos entre trabajos y materiales.

### Detalle_Pedido
Tabla intermedia que permite registrar múltiples materiales por pedido, incluyendo la cantidad de cada uno.

---

## Decisiones de diseño

- Los pedidos no se relacionan directamente con los trabajos debido a que los materiales se adquieren en mayoreo.
- Se utilizaron claves compuestas en las tablas intermedias para garantizar la unicidad.
- Se eliminaron atributos redundantes para cumplir con la tercera forma normal.

---

