BASE DE DATOS CSV REALISTA — MotoRide Group

Tablas incluidas:
1. clientes.csv    → 500 clientes
2. productos.csv   → 20 productos reales de temática motos
3. vendedores.csv  → 20 vendedores asignados a tiendas
4. tiendas.csv     → 10 tiendas
5. ventas.csv      → 6000 ventas

Relaciones recomendadas:

clientes[cliente_id]       (1) ─── (*) ventas[cliente_id]
productos[producto_id]     (1) ─── (*) ventas[producto_id]
vendedores[vendedor_id]    (1) ─── (*) ventas[vendedor_id]
tiendas[tienda_id]         (1) ─── (*) ventas[tienda_id]

Además:
tiendas[tienda_id]         (1) ─── (*) vendedores[tienda_id]

Notas:
- Las motos tienen cantidad 1 en cada venta.
- Accesorios, ropa y recambios pueden tener cantidades de 1 a 4.
- Los importes se calculan a partir del precio del producto con descuentos realistas.
- Los vendedores están vinculados a una tienda.
