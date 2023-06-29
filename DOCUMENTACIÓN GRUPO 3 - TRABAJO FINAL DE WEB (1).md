### Integrantes
* Villa Mera, Jasmin
* Chavez Sanchez, Jose Raul
* Fernandez Alva, Edu

### TABLA: USUARIO


| Columna | Tipo de dato |
| -------- | -------- |
|**id_usuario**	|Integer |
|**Nombres**	|varchar(30)|
|**Apellido**	|varchar(40)|
|**Email**|varchar(60)|
|**Contraseña**|varchar(30)|
|**Telefono**|varchar(11)|
|**Tipo**|char(1)|
|**Vigencia**|boolean|



#### Obtener Usuario

|Nombre	|Obtener Usuario|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	 team03.pythonanywhere.com/api_obtenerusuarios|

##### Response 

```
[
    {
        "apellido": "fernandez",
        "contraseña": "edu123",
        "email": "edu8@gmail.com",
        "id_usuario": 2,
        "nombre": "edu",
        "telefono": "912203789",
        "tipo": "V",
        "vigencia": "Vigente"
    }
]
```


#### Obtener Usuario Por ID


|**Nombre**|	Obtener Usuario por ID|
| -------- | -------- |
|**Método**|	GET|
|**URL**|	team03.pythonanywhere.com/api_obtenerusuario/2|
##### Response
```
    {
        "apellido": "fernandez",
        "contraseña": "edu123",
        "email": "edu8@gmail.com",
        "id_usuario": 2,
        "nombre": "edu",
        "telefono": "912203789",
        "tipo": "V",
        "vigencia": 1
    }

```

#### Guardar Usuario
|**Nombre**|	Guardar Usuario|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_guardarusuario|


##### Request
```
        {
            "nombres": "edu",
            "apellido": "fernandez",
            "email": "edu8@gmail.com",
            "contraseña": "edu123",
            "telefono": "912203789",
            "tipo": "V"
            "nombre_usuario": "admin"
        }
```

##### Response	

```
{
    "Mensaje": "usuario registrado correctamente"
}
```

#### Actualizar Usuario
|**Nombre**|	Actualizar Usuario|
| -------- | -------- |
|**Método**|	POST|
|**URL**|	team03.pythonanywhere.com/api_actualizarusuario|

##### Request	
        {
            "id_usuario": 4,
            "nombres": "Pedro",
            "apellido": "Nuñez Perez",
            "email": "n@gmail.com",
            "contraseña": "123456789",
            "telefono": "912203700",
            "tipo": "C",
            "vigencia": 1,
            "nombre_usuario": "pepe001"
        }

##### Response	
```
{
    "Mensaje": "usuario actualizado correctamente"
}
```

#### Eliminar Usuario
|**Nombre**	|Eliminar Usuario|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_eliminarusuario|



##### Request	

```
{
    "id_usuario" : 3
}
```

##### Response	

```
{
    "Mensaje": "Usuario eliminado correctamente"
}
```
### TABLA: CLIENTE


| Columna | Tipo de dato |
| -------- | -------- |
|**id_cliente**|Integer|
|**Nombres**|varchar(30)|
|**Apellido**|varchar(40)|
|**DNI**|vachar(8)|
|**Email**|varchar(60)|
|**Telefono**|varchar(11)|
|**Vigencia**|boolean|

#### Obtener Cliente

|Nombre	|Obtener Cliente|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	 team03.pythonanywhere.com/api_obtenerclientes|

##### Response 

```
[
    {
        "apellido": "Villa Mera",
        "dni": "76937008",
        "email": "xxxxxxxx@gmail.com",
        "id_cliente": 3,
        "nombres": "Jasmin Elizaaa",
        "telefono": "902430969",
        "vigencia": "No Vigente"
    },
    {
        "apellido": "Villa Mera",
        "dni": "43724679",
        "email": "jasminvm@gmail.com",
        "id_cliente": 6,
        "nombres": "Jasmin",
        "telefono": "902430969",
        "vigencia": "Vigente"
    }
]
```


#### Obtener Cliente Por ID


|**Nombre**|	Obtener Cliente por Id|
| -------- | -------- |
|**Método**|	GET|
|**URL**|	team03.pythonanywhere.com/api_obtenercliente/3
##### Response
```
[
    {
        "apellido": "Villa Mera",
        "dni": "76937008",
        "email": "xxxxxxxx@gmail.com",
        "id_cliente": 3,
        "nombres": "Jasmin Elizaaa",
        "telefono": "902430969",
        "vigencia": 0
    }
]

```

#### Guardar Cliente
|**Nombre**|	Guardar Cliente|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_guardarcliente|


##### Request
```
    {
        "nombres" : "Jose",
        "apellido" : "Chavez Sanchez",
        "dni" : "71116809",
        "email" : "joseraulchavezsanchez12345678@gmail.com",
        "telefono" : "978420505"
    }

```

##### Response	

```
{
    "Mensaje": "cliente registrado correctamente"
}
```
---
#### Actualizar Cliente
|**Nombre**|	Actualizar Cliente|
| -------- | -------- |
|**Método**|	POST|
|**URL**|	team03.pythonanywhere.com/api_actualizarcliente|

##### Request	
```
    {
        "id_cliente" : "3",
        "nombres" : "Jasmin Elizaaa",
        "apellido" : "Villa Mera",
        "dni" : "76937008",
        "email" : "xxxxxxxx@gmail.com",
        "telefono" : "902430969",
        "vigencia" : 0
    }
```
##### Response	
```
{
    "Mensaje": "Cliente actualizado correctamente"
}
```

#### Eliminar Cliente
|**Nombre**	|Eliminar Cliente|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_eliminarcliente|



##### Request	

```
    {
        "id_cliente": 5
    }
```

##### Response	

```
{
    "Mensaje": "Cliente eliminado correctamente"
}
```

### TABLA: METODO DE PAGO


| Columna | Tipo de dato |
| -------- | -------- |
|**id_metodo_pago**|Integer|
|**Nombre**|varchar(30)|
|**Vigencia**|Boolean|

#### Obtener Metodo de Pago

|Nombre	|Obtener Metodo de Pago|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	team03.pythonanywhere.com/api_obtenermetodopagos|

##### Response 

```
[
    {
        "id_metodo_pago": 1,
        "nombre": "efectivo",
        "vigencia": "No Vigente"
    }
]
```


#### Obtener Metodo de Pago Por ID


|**Nombre**|	Obtener Metodo de Pago por Id|
| -------- | -------- |
|**Método**|	GET|
|**URL**|team03.pythonanywhere.com/api_obtenermetodopago/1|
##### Response
```
[
    {
        "id_metodo_pago": 1,
        "nombre": "efectivo",
        "vigencia": 0
    }
]

```
---
#### Guardar Metodo de Pago
|Nombre|	Guardar Metodo de Pago|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|	team03.pythonanywhere.com/api_guardarmetodopago|


##### Request
```
{
    "nombre" : "credito"

}
```

##### Response	

```
{
    "Mensaje": "Metodo pago registrado correctamente"
}
```
---
#### Actualizar Metodo de Pago
|**Nombre**|	Actualizar Metodo de Pago|
| -------- | -------- |
|**Método**|	POST|
|**URL**|team03.pythonanywhere.com/api_actualizarmetodopago|

##### Request	
```
        {
            "id_metodo_pago": 1,
            "nombre": "efectivo",
            "vigencia": 0
        }
```
##### Response	
```
{
    "Mensaje": "Metodo pago actualizado correctamente"
}
```

#### Eliminar Metodo de Pago
|Nombre	|Eliminar Metodo de Pago|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|	team03.pythonanywhere.com/api_eliminarmetodopago|



##### Request	

```
{
    "id_metodo_pago" : "2"
}
```

##### Response	

```
{
    "Mensaje": "Metodo de pago eliminado correctamente"
}
```

### TABLA: TIPO DE VENTA
|Columna| Tipo de dato|
| -------- | -------- |
|**id_tipo_venta**|Integer|
|**Nombre**|varchar(30)|
|**Vigencia**|Boolean|

#### Obtener Tipo de Venta


|**Nombre**|Obtener Tipo de Venta|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenertipoventa|
##### Response 
```
[
    {
        "id_tipo_venta": 1,
        "nombre": "directa",
        "vigencia": "No Vigente"
    }
]
```
#### Obtener Tipo de Venta por ID


|**Nombre**| Obtener Tipo de Venta por ID|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenertipoventa/1|
##### Response 
```
[
    {
        "id_tipo_venta": 1,
        "nombre": "directa",
        "vigencia": 0
    }
]
```

#### Guardar Tipo de Venta


|**Nombre**| Guardar Tipo de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_guardartipoventa|
##### Request 
```
{
    "nombre" : "directa"
}
```
##### Response 
```
{
    "Mensaje": "Tipo venta registrada correctamente"
}
```


#### Actualizar Tipo de Venta

|**Nombre**| Actualizar Tipo de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_actualizartipoventa|
##### Request 
```
    {
        "id_marca": 5,
        "nombre": "nike",
        "vigencia": 0
    }
```
##### Response 
```
{
    "Mensaje": "Tipo venta actualizada correctamente"
}
```
#### Eliminar Tipo de Venta

|**Nombre**| Eliminar Tipo de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_eliminartipoventa|
##### Request 
```
{
    "id_tipo_venta" : "2"
}
```
##### Response 
```
{
    "Mensaje": "Tipo venta eliminada correctamente"
}
```

### TABLA: MARCA


| Columna | Tipo de dato |
| -------- | -------- |
|**id_marca**	|Integer |
|**Nombre**	|varchar(30)|
|**Vigencia**|boolean|



#### Obtener Marca

|Nombre	|Obtener Marca|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	 team03.pythonanywhere.com/api_obtenermarcas|

##### Response 

```
[
    {
        "id_marca": 1,
        "nombre": "adidas",
        "vigencia": "Vigente"
    },
    {
        "id_marca": 2,
        "nombre": "nike",
        "vigencia": "Vigente"
    }
]
```


#### Obtener Marca Por ID


|**Nombre**|	Obtener Marca por ID|
| -------- | -------- |
|**Método**|	GET|
|**URL**|	team03.pythonanywhere.com/api_obtenermarca/3|
##### Response
```
[
  {
    "id_marca": 3,
    "nombre": "puma",
    "vigencia": 1
  }
]

```

#### Guardar Marca
|**Nombre**|	Guardar Marca|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_guardarmarca|


##### Request
```
    {
        "nombre": "puma"
    }
```

##### Response	

```
{
    "Mensaje": "Marca registrada correctamente"
}
```

#### Actualizar Marca
|**Nombre**|	Actualizar Marca|
| -------- | -------- |
|**Método**|	POST|
|**URL**|	team03.pythonanywhere.com/api_actualizarmarca|

##### Request	
 {
        "id_marca": 2,
        "nombre": "adidas",
        "vigencia": 0
}

##### Response	
```
{
    "Mensaje": "Marca actualizada correctamente"
}
```

#### Eliminar Marca
|**Nombre**	|Eliminar Marca|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_eliminarmarca|



##### Request	

```
    {
        "id_marca": 2
    }
```

##### Response	

```
{
    "Mensaje": "Marca eliminada correctamente"
}
```
### TABLA: CATEGORIA


| Columna | Tipo de dato |
| -------- | -------- |
|**id_categoria**|Integer|
|**Nombre**|varchar(30)|
|**Vigencia**|boolean|

#### Obtener Categoria

|Nombre	|Obtener Categoria|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	 team03.pythonanywhere.com/api_obtenercategorias|

##### Response 

```
[
    {
        "id_categoria": 1,
        "nombre": "fiesta",
        "vigencia": "Vigente"
    }
]
```


#### Obtener Categoria Por ID


|**Nombre**|	Obtener Categoria por Id|
| -------- | -------- |
|**Método**|	GET|
|**URL**|	team03.pythonanywhere.com/api_obtenercategoria/1
##### Response
```
[
    {
        "id_categoria": 1,
        "nombre": "fiesta",
        "vigencia": 1
    }
]

```

#### Guardar Categoria
|**Nombre**|	Guardar Categoria|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_guardarcategoria|


##### Request
```
    {
        "nombre": "elegante"
    }


```

##### Response	

```
{
    "Mensaje": "Categoria registrada correctamente"
}
```
---
#### Actualizar Categoria
|**Nombre**|	Actualizar Categoria|
| -------- | -------- |
|**Método**|	POST|
|**URL**|	team03.pythonanywhere.com/api_actualizarcategoria|

##### Request	
```
    {
        "id_categoria": 1,
        "nombre": "fiestas",
        "vigencia": 1
    }
```
##### Response	
```
{
    "Mensaje": "Categoria actualizada correctamente"
}
```

#### Eliminar Categoria
|**Nombre**	|Eliminar Categoria|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|team03.pythonanywhere.com/api_eliminarcategoria|



##### Request	

```
{
        "id_categoria": 3

}
```

##### Response	

```
{
    "Mensaje": "Categoria eliminada correctamente"
}
```

### TABLA: PRODUCTO


| Columna | Tipo de dato |
| -------- | -------- |
|**id_producto**|Integer|
|**id_marca**|Integer|
|**id_categoria**|Integer|
|**nombre**|varchar(40)|
|**descripcion**|varchar(150)|
|**precio**|numeric(10,2)|
|**stock**|Integer|
|**modelo**|varchar(30)|
|**vigencia**|boolean|

#### Obtener Producto

|Nombre	|Obtener Producto|
| -------- | -------- | 
|**Método**	|GET|
|**URL**|	team03.pythonanywhere.com/api_obtenerproductos|

##### Response 

```
[
    {
        "descripcion": "de cuero",
        "id_producto": 1,
        "marca_id": "adidas",
        "modelo": "",
        "nombre": "chanclas",
        "precio ": "60.00",
        "stock": 100,
        "vigencia": "Vigente"
    }
]
```


#### Obtener Producto Por ID


|**Nombre**|	Obtener Producto por Id|
| -------- | -------- |
|**Método**|	GET|
|**URL**|team03.pythonanywhere.com/api_obtenerproducto/1|
##### Response
```
[
    {
        "descripcion": "de cuero",
        "id_producto": 1,
        "marca_id": 1,
        "modelo": "",
        "nombre": "chanclas",
        "precio ": "60.00",
        "stock": 100,
        "vigencia": 1
    }
]

```
---
#### Guardar Producto
|Nombre|	Guardar Producto|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|	team03.pythonanywhere.com/api_guardarproducto|


##### Request
```
{
    "nombre" : "chanclas",
    "descripcion" : "de cuero",
    "precio" : "60",
    "stock" : "100",
    "modelo" : "" ,
    "marca_id" : "1",
    "categoria_id" : "1"
}
```

##### Response	

```
{
    "message": "Producto registrado correctamente",
    "status": "1"
}
```
---
#### Actualizar Producto
|**Nombre**|	Actualizar Producto|
| -------- | -------- |
|**Método**|	POST|
|**URL**|team03.pythonanywhere.com/api_actualizarproducto|

##### Request	
```
{
    "id_producto" : "1",
    "nombre" : "zapatos",
    "descripcion" : "bamba",
    "precio" : "70",
    "stock" : "100",
    "modelo" : "ddd" ,
    "marca_id" : "1",
    "categoria_id" : "1",
    "vigencia" : "true"

}
```
##### Response	
```
{
    "message": "Producto actualizado correctamente",
    "status": "1"
}
```

#### Eliminar Producto
|Nombre	|Eliminar Producto|
| -------- | -------- |
|**Método**	|POST|
|**URL**	|	team03.pythonanywhere.com/api_eliminarproducto|



##### Request	

```
{
    "id_producto" : "2"

}
```

##### Response	

```
{
    "Mensaje": "Producto eliminado correctamente"
}
```

### TABLA: VENTA
|Columna| Tipo de dato|
| -------- | -------- |
|**id_metodo_pago**|Integer|
|**id_cliente**|Integer|
|**id_usuario**|Integer|
|**id_tipo_venta**|Integer|
|**fecha**|date|
|**total**|numeric(10,2)|

#### Obtener Venta


|**Nombre**|Obtener Venta|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenerventas|
##### Response 
```
[
    {
        "cliente_id": 3,
        "fecha": "Sat, 17 Jun 2023 00:00:00 GMT",
        "id_venta": 1,
        "metodo_pago_id": 1,
        "total": "100.00",
        "usuario_id": 2
    }
]
```
#### Obtener Venta por ID


|**Nombre**| Obtener Venta por ID|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenerventa/1|
##### Response 
```
[
    {
        "cliente_id": 3,
        "fecha": "Sat, 17 Jun 2023 00:00:00 GMT",
        "id_venta": 1,
        "metodo_pago_id": 1,
        "total": "100.00",
        "usuario_id": 2
    }
]
```

#### Guardar Venta


|**Nombre**| Guardar Tipo de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_guardarventa|
##### Request 
```
{
    "cliente_id" : 3,
    "metodo_pago_id" : 1,
    "tipo_venta_id" : 1,
    "usuario_id" : 2,
    "fecha" : "2023-06-17",
    "total" : "100.00" 
}
```
##### Response 
```
{
    "message": "Venta registrada correctamente",
    "status": "1"
}
```


#### Actualizar Venta

|**Nombre**| Actualizar Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_actualizarventa|
##### Request 
```
    {
        "id_venta" : 2,
        "cliente_id": 3,
        "metodo_pago_id": 1,
        "tipo_venta_id":1,
        "usuario_id": 2,
        "fecha": "2023-06-01",
        "total": 120.00
    }
```
##### Response 
```
{
    "Mensaje": "Tipo venta actualizada correctamente"
}
```
#### Eliminar Venta

|**Nombre**| Eliminar Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_eliminarventa|
##### Request 
```
{
    "id_venta" : 2
}
```
##### Response 
```
{
    "Mensaje": "Venta eliminada correctamente"
}
```
### TABLA: DETALLE VENTA
|Columna| Tipo de dato|
| -------- | -------- |
|**id_venta**|Integer|
|**id_producto**|Integer|
|**cantidad**|Integer|
|**precio_unitario**|numeric(10,2)|
|**subtotal**|numeric(10,2)|

#### Obtener Detalle de Venta


|**Nombre**|Obtener Detalle de Venta|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenerdetalleventas|
##### Response 
```
[
    {
        "cantidad": 2,
        "precio_unitario": "60.00",
        "producto_id": 1,
        "subtotal": "120.00",
        "venta_id": 1
    }
]
```
#### Obtener Detalle de Venta por ID


|**Nombre**| Obtener Venta por ID|
| -------- | -------- | 
|**Método**|GET|
|**URL**|team03.pythonanywhere.com/api_obtenerdetalleventa/1/1|
##### Response 
```
[
    {
        "cantidad": 2,
        "precio_unitario": "60.00",
        "producto_id": 1,
        "subtotal": "120.00",
        "venta_id": 1
    }
]
```

#### Guardar Detalle de Venta


|**Nombre**| Guardar Detalle de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_guardardetalleventa|
##### Request 
```
{
        "venta_id": 1,
        "producto_id" : 1,
        "cantidad": 2,
        "precio_unitario" : 60.00,
        "subtotal" : 120.00
}
```
##### Response 
```
{
    "message": "Detalle de Venta registrada correctamente",
    "status": "1"
}
```


#### Actualizar Detalle de Venta

|**Nombre**| Actualizar Detalle de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_actualizardetalleventa|
##### Request 
```
{
        "venta_id": 1,
        "producto_id" : 1,
        "cantidad": 2,
        "precio_unitario" : 70.00,
        "subtotal" : 150.00
}
```
##### Response 
```
{
    "Mensaje": "Detalle venta actualizada correctamente"
}
```
#### Eliminar Detalle de Venta

|**Nombre**| Eliminar Detalle de Venta|
| -------- | -------- | 
|**Método**|POST|
|**URL**|team03.pythonanywhere.com/api_eliminardetalleventa|
##### Request 
```
{
        "venta_id": 2,
        "producto_id" : 1
}
```
##### Response 
```
{
    "Mensaje": "Detalle Venta eliminada correctamente"
}
```