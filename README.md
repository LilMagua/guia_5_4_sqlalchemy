```
¿Qué parte de la aplicación conoce ahora la estructura de la tabla estudiantes?
El archivo "models.py" es el encargado de crear la tabla y cada una de sus columnas, definiendo llave primaria, tipo de dato, longitud, si puede ser vacio o no, ademas tiene un metodo __repr__ para definir como se representara en texto.

¿Qué diferencia existe entre crear un objeto Estudiante y hacerlo persistente en la base de datos?
Crear un objeto estudiante unicamente lo crea en el tiempo de ejecucion del programa, lo que hace que no se mantenga una vez cerrado, hacerlo persistente mediante el ORM de python lo guarda de manera permanente.

¿Qué función cumple commit() dentro de una sesión?
Commit ejecuta la operacion correspondiente en la base de datos, ejemplo
        # "Quiero que este objeto se guarde en la base de datos."
        session.add(estudiante)
        # SQLAlchemy ejecuta la operación correspondiente en la base de datos
        '''
        Es como realizar
        INSERT INTO estudiantes (nombre, correo, nota)
        VALUES ('Ana', 'ana@mail.com', 4.5);
        '''

¿Por qué una restricción UNIQUE sigue siendo importante aunque se utilice un ORM?
Porque el ORM debe seguir diciendole de forma clara a la base de datos si un dato debe ser unico o no.

¿Qué ventajas tendría esta separación si el sistema incorporara nuevas entidades y relaciones?
Que se pueden seguir manejando como objetos del paradigma de programacion "Orientado a objetos" sin necesidad de incluir consultas SQL directamente en el codigo.
```