#### 1. Inserción de datos

- INSERT INTO fabricante VALUES

   (1, 'Asus'),

  (2, 'Lenovo'),

  (3, 'Hewlett-Packard'),

  (4, 'Samsung'),

  (5,'Seagate'),

  (6,'Crucial'),

  (7, 'Gigabyte'),

  (8, 'Huawei'),

  (9, ' Xiaomi');

- INSERT INTO producto VALUES

   (1, 'Disco duro SATA3 1TB', 86.99, 5),

  (2, 'Memoria RAM DDR4 8GB', 150.99, 4),

  (3, 'Disco SSD 1 TB', 150.99, 4),

  (4, 'GeForce GTX 1050Ti, 185, 7),

  (5,'GeForce GTX 1080 Xtreme, 755, 6),

  (6,'Monitor 24 LED Full HD', 202, 1),

  (7, 'Monitor 27 LED Full HD', 245.99, 1),

  (8, 'Portátil Yoga 520', 599, 2),

  (9, ' Portátil Ideapd 320', 444, 2),

  (10, 'Impresora HP Deskjet 3720', 59.99, 3),

  (11, 'Impresora HP Laserjet Pro M26nw', 180, 3);

#### 2. Consultas sobre una tabla

1. Lista el nombre de todos los productos que hay en la tabla producto.

​	**SELECT nombre FROM producto**;

2. Lista los nombres y los precios de todos los productos de la tabla producto.

​	**SELECT nombre, precio FROM producto**;

3. Lista todas las columnas de la tabla producto.

​	**SELECT nombre, precio, codigo_fabricante FROM producto**;

4. Lista el nombre de los productos, el precio en euros y el precio en dólares

​	estadounidenses (USD).

​	**SELECT nombre, precio, precio * 1.07 AS precio_dolares FROM producto**;

5. Lista el nombre de los productos, el precio en euros y el precio en dólares
   estadounidenses (USD). Utiliza los siguientes alias para las columnas: nombre
   de producto, euros, dólares.

​	**SELECT nombre AS nombre de producto, precio AS euros, precio * 1.07 AS dólares FROM producto**;

6. Lista los nombres y los precios de todos los productos de la tabla producto, convirtiendo los nombres a mayúscula.

   **SELECT UPPER(nombre), precio FROM producto**;

7. Lista los nombres y los precios de todos los productos de la tabla producto, convirtiendo los nombres a minúscula.

   **SELECT LOWER(nombre), precio FROM producto**;

8. Lista el nombre de todos los fabricantes en una columna, y en otra columna obtenga en mayúsculas los dos primeros caracteres del nombre del fabricante.

​	**SELECT nombre, UPPER(SUBSTRING(nombre, 1,2)) FROM fabricante**;

9. Lista los nombres y los precios de todos los productos de la tabla producto, redondeando el valor del precio.

​	**SELECT nombre, ROUND(precio, 0);**

10. Lista los nombres y los precios de todos los productos de la tabla producto, truncando el valor del precio para mostrarlo sin ninguna cifra decimal.

​	**SELECT nombre, TRUNCATE(precio, 0);**

11.  Lista el identificador de los fabricantes que tienen productos en la tabla producto.

​	**SELECT codigo_fabricante FROM producto**

12. Lista el identificador de los fabricantes que tienen productos en la tabla producto, eliminando los identificadores que aparecen repetidos.

​	**SELECT DISTINCT codigo_fabricante FROM producto**

13. Lista los nombres de los fabricantes ordenados de forma ascendente.

    **SELECT nombre FROM fabricante**

    **ORDER BY nombre;**

14. Lista los nombres de los fabricantes ordenados de forma descendente.

​	**SELECT nombre FROM fabricante**

​	**ORDER BY nombre ASC;**

15. Lista los nombres de los productos ordenados en primer lugar por el nombre de forma ascendente y en segundo lugar por el precio de forma descendente.

​	**SELECT nombre FROM fabricante**

​	**ORDER BY nombre ASC**,

​	**ORDER BY precio DESC;** 

16. Devuelve una lista con las 5 primeras filas de la tabla fabricante.

​	**SELECT TOP 5  codigo, nombre FROM fabricante**;

17. Devuelve una lista con 2 filas a partir de la cuarta fila de la tabla fabricante. La cuarta fila también se debe incluir en la respuesta.

​	**SELECT * FROM fabricante OFFSET 3 LIMIT 2;**