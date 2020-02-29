# SwiftProject
**Swift Project**

Este proyecto utiliza tecnologia de **Pods** para un **tabBar**, un **login** gracias a google y **RealmSwift** que se encargara de  CRUD  tambien este proyecto tiene **TableView** para mostrar los datos de **RealmSwift**



**Partes destacables** 

En el siguiente código veremos como usamos el login de Google, si el usuario que intenta acceder a la aplicación y no tiene su sesión iniciada mandaremos al login de Google
si pasa la autenticación de Google mandaremos al mainControler de la app en este caso sera EventView

![image-20200226192040301](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200226192040301.png)



También una parte importante del codigo es TabBAr, en nuestro caso usamos Pods

![image-20200229213658343](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229213658343.png)

![image-20200229213752728](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229213752728.png)

lo que hace este código es inicializar cada  ViewControler para poder usarlo y cambiarlo en el tabBAr 

![image-20200229213948295](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229213948295.png)

las flechas indican que icono de imagen tendrán cada opción del TabBar 

![image-20200229214126109](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229214126109.png)

cada clase tendra que ser extendida de UIViewController para poder ser usada en TabBarItem



Cuando se inicia la aplicacion y el usuario cambia de pantalla en cada ViewControler tenemos  el siguiente formato para mostrar los datos de Realm

Primero se instancia la base de datos RealmSwift atreves de una clase que es manager con un constructor privado:

![image-20200229214856071](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229214856071.png)

como vemos cuando se instancia RealmSwift y es primera vez que se llama al constructor y se cargaran los datos en RealmSwift para ver resultados en la aplicación despues de saber como funciona el constructor veremos como cargamos los datos



![image-20200229214350707](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229214350707.png)

como vemos en la imagen se llama al constructor luego solicitamos datos con una funcion que tiene al archivo Manager que lo que hace es cargar todos los datos de los ciclistas 



![image-20200229220033430](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229220033430.png)

luego recorremos los resultados con un bucle y cargamos todos los datos en memoria para usarlo en un table view



![image-20200229220439636](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229220439636.png)

para poder usar tableView tendremos que añadir un tableView a nuestro achivo .xib y capturarlo par luego delegarlo en nuestra clase donde queremos usarlo

![image-20200229220539305](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229220539305.png)



y por defecto tenemos que usar 2 funciones necesarias:

![image-20200229220637618](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229220637618.png)

lo que hace esto es que en la tabla el tamaño de cada sección y cuantas filas abra 

y con otra función daremos valor a cada sección con los datos que recuperamos de RealmSwift

![image-20200229220855491](https://github.com/kiwiStucom/SwiftProject/blob/master/img/image-20200229220855491.png)
