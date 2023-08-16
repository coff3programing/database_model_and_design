# Formulario

## Listado de atributos

### registro **(EP)**

- id **(PK)**
- fecha
- usuario **(FK)**
- direccion **(FK)**

### usuario **(ED)**

- id_usuario **(PK)**
- id_documento **(FK)**
- numero_documento **(UK)**
- nombre
- apellido
- correo **(UK)**
- id_telefono **(FK)**
- telefono

### telefono **(EC)**

- id_telefono **(PK)**
- tipo_telefono **(UK)**

### documentos_de_identidad **(EC)**

- id_documento **(PK)**
- tipo_documento **(UK)**
- rp_vulnerabilidad

### direccion **(ED)**

- id_direccion **(PK)**
- id_usuario **(FK)**
- calle_principal
- calle_transversal
- id_parroquia **(FK)**

### parroquia **(ED|EC)**

- id_parroquia **(PK)**
- parroquia
- tipo_parroquia
- id_sector **(FK)**

### sector **(EC)**

- id_sector **(PK)**
- sector

## Relaciones

1. Un **registro** llenado **usuario** (_1 - 1_)
2. Un **usuario** tiene **telefono** (_1 - 1_)
3. Un **usuario** tiene **Documentos de identidad** (_1 - 1_)
4. Una **direccion** pertenece **usuario** (_1 - 1_ )
5. Una **direccion** tiene **parroquia** (_1 - 1_)
6. Una **parroquia** posee **sector** (_1 - M_)

## Logica de Negocio

### usuario

1. Registrar los datos de un usuario.
2. Leer todos los usuarios.
3. Leer un usuario en particular.
4. Actualizar un usuario.
5. Eliminar un usuario.

### dirección

1. Crear una parroquia.
2. Leer todos los barrios de la parroquia.
3. Leer un barrio en particular
4. Actualizar una parroquia.
5. Eliminar una parroquia.

### MODELOS RELACIONALES

![Modelo Relacional](modelo%20relacional%20de%20la%20base%20de%20datos.drawio.png)
