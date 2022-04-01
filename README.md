# Clausula Where Oracle
#### Consultar datos de nuestra tabla utilizando la clausula where, esta clausula nos permite discriminar por un dato en especifico alguna consulta que necesitemos de alguna tabla.

```sql
 create table articulos(
  codigo number(5),
  nombre varchar2(20),
  descripcion varchar2(30),
  precio number(7,2)
 );
 ```
 
 ```sql
 insert into articulos values (1,'impresora','Epson Stylus C45',400.80);
 insert into articulos values (2,'impresora','Epson Stylus C85',500);
 insert into articulos values (3,'monitor','Samsung 14',800);
 ```
 
 ```sql
 select * from articulos;
 ```
 
 | CODIGO            | NOMBRE           |  DESCRIPCION   |   PRECIO   |
 | ------------------|:----------------:|---------------:|-----------:|
 | 1            | impresora           |  Epson Stylus C45   |   400.80   |
 | 2            | impresora           |  Epson Stylus C85   |   500   |
 | 3            | monitor           |  Samsung 14   |   800   |
 
 #### Consulta con where
  ```sql
 select * from articulos where nombre = 'impresora';
 ```
 #### Resultado: 
 | CODIGO            | NOMBRE           |  DESCRIPCION   |   PRECIO   |
 | ------------------|:----------------:|---------------:|-----------:|
 | 1            | impresora           |  Epson Stylus C45   |   400.80   |
 | 2            | impresora           |  Epson Stylus C85   |   500   |

 
> consulta con campos especificos utilizando where
 ```sql
 select nombre, descripcion from articulos where nombre = 'impresora';
 ```
  #### Resultado: 
  
| NOMBRE           |  DESCRIPCION   |
|:----------------:|---------------:|
| impresora           |  Epson Stylus C45   |
| impresora           |  Epson Stylus C85   |
