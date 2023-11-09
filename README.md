# Ing-software1
Repositorio de la materia "Ingenieria de Software 1" unlp 2023

### Links que me ayudaron a aprobar la materia:
-Repositorio de agusrnfr con ejercicios y parciales:  
https://github.com/agusrnfr/ING-1/tree/main

-Google docs para hacer historias de usuario y casos de uso:  
https://docs.google.com/

-Draw.io para hacer diagramas de cu, dte y redes de petri:  
https://app.diagrams.net/

### Dudas resueltas que fueron surgiendo mientras hacia las practicas:
#### Practica 2 Historias de usuario:
-¿Que va en el dado? RTA: en el dado van las VALIDACIONES, cosas que tenemos que validar (siempre validaciones a nivel de negocio osea, no se validan cosas como por ej si el cliente ingresa su mail sin @ o si no puso .com al final etc), en el cuando si va todos los datos completos. En el DADO hay que poner cosas que ya pasaron o condiciones que ya son verdaderas/falsas, no puedo poner cosas que podrian pasar o que el usuario haria en un futuro en el CUANDO por ej: "DADO que el usuario seleccionaria una foto valida" esta mal.

-Si en el DADO una validacion depende de una anterior por ej clave depende de que un nombre de usuario sea valido, si quiero validar que el nombre de usuario no es valido, no hace falta escribir que la clave es valida porque el nombre de usuario no existe por lo tanto es imposible que la clave sea valida.

-Si tengo una historia de iniciar sesion y varios roles la usan, ¿esta bien tener 2 escenarios exitosos si el dado o el entonces es distinto? RTA: si, ademas dependiendo el sistema puedo tener 2 escenarios fallidos, 1 por usuario incorrecto y otro por clave, o un solo escenario general donde no se controla que es lo incorrecto del inicio de sesion (es mas expresivo hacer 2 escenarios).

#### Practica 3 Casos de uso:
-Pregunta generica: ¿Las precondiciones son cuando el sistema puede de antemano verificarlo? 
RTA: si. Se puede pensar como que cuando las precondiciones no se cumple entonces el boton de la interfaz que permite ejecutar ese CU esta deshabilitado. Las cosas que se verifican en el mismo cu no pueden ser precondiciones.

-Se pueden tener 2 pasos alternativos al mismo paso? RTA: SE PUEDE PERO EVITAR, generalmente si tenes que tener 2 pasos alternativos al mismo paso algo estas haciendo raro.

-Se puede en un paso alternativo volver a un paso que todavia no paso? RTA: SI, en el paso alternativo 4 se puede retornar al paso 7.

-Generalmente, los pasos alternos casi siempre son del sistema, exceptuando los casos en donde el actor tiene que aceptar/rechazar algo, en ese caso se puede tener en curso normal que el actor acepta y en caso alterno que el actor rechaza y fin de cu, pero si no, casi siempre los cursos alternos son del sistema.

-Generalmente, cuando un caso alternativo te lleva a los primeros pasos, casi siempre es lo mismo retornar que finalizar el CU.

-Se usan depends? no hice ninguno RTA: porque no hay en la practica, en la practica se representan los depends con precondiciones.

-Pregunta genérica: ¿es necesario poner todos los campos que el usuario tiene que ingresar? RTA: Es necesario ponerlo del lado del sistema pero no del lado del usuario, con poner "El usuario ingresa los datos correspondientes" bastaría.

-Cuando por ejemplo tengo que mostrar una lista y esa lista por x motivo puede quedar vacia, contemplar poner un paso alterno que informe que no hay nada que poner en la lista por x razon.

-Cuando un cu es USES de otros 2 o mas cus en precondiciones va "Se debe haber ejecutado el CU “cu1” o “cu2”." mas que nada para "justificar" que el primer paso lo da el sistema.

-La flecha de herencia apunta de un actor a DE QUIEN hereda, osea podriamos decir actor 2 hereda de (flechita a) actor 1, actor 2 ES UN actor 1.

#### Practica 5 Redes de Petri:

-¿Una transición puede tener dos acciones en el nombre? RTA: Si se puede, por ejemplo, "Terminar de firmar y se retira".

-Es conveniente que las transiciones finales solo reciban un arco.

-No es lo mismo despachar un GRUPO de 4 cajas que despachar por ejemplo UN PAQUETE con 4 cajas adentro, porque un grupo de 4 cajas es igual a 4 cajas juntas (4 tokens), UN paquete (un token) que tiene adentro 4 cajas no es lo mismo que 4 cajas juntas y nada mas.

<p align="center">
    <img src= "https://i.postimg.cc/RFj3cHcM/1.jpg" alt = "img1"/>
</p>