# Ing-software1
Repositorio de la materia "Ingenieria de Software 1" unlp 2023.  
Las practicas 4 y 5 (Dte y RP) tienen todos los puntos corregidos por ayudantes, las practicas 1, 2 y 3 no alcance a completar y corregirlos todos.

### Links utiles para la materia:
-Repositorio de agusrnfr con ejercicios y parciales:  
https://github.com/agusrnfr/ING-1/tree/main

-Google docs para hacer historias de usuario y casos de uso:  
https://docs.google.com/

-Draw.io para hacer diagramas de cu, dte y redes de petri:  
https://app.diagrams.net/

-Explicaciones y ejercicios resultos en practica 2021:  
https://drive.google.com/drive/u/0/folders/1UjJ1wP89T-SJTLf9fQrORbh36o_PUjWe

-Consultas practicas grabadas 2021:  
https://www.youtube.com/playlist?list=PLeVhd2SrgCdTqQ-MD40JMRzXP57YcDVXb

### Dudas resueltas que fueron surgiendo mientras hacia las practicas:
#### Practica 2 Historias de usuario:
-¿Que va en el dado? RTA: en el dado van las VALIDACIONES, cosas que tenemos que validar (siempre validaciones a nivel de negocio osea, no se validan cosas como por ej si el cliente ingresa su mail sin @ o si no puso .com al final etc), en el cuando si va todos los datos completos. En el DADO hay que poner cosas que ya pasaron o condiciones que ya son verdaderas/falsas, no puedo poner cosas que podrían pasar o que el usuario haría en un futuro en el CUANDO por ej: "DADO que el usuario seleccionaria una foto válida" esta mal.

-Si en el DADO una validación depende de una anterior por ej clave depende de que un nombre de usuario sea válido, si quiero validar que el nombre de usuario no es válido, no hace falta escribir que la clave es válida porque el nombre de usuario no existe por lo tanto es imposible que la clave sea válida.

-Si tengo una historia de iniciar sesión y varios roles la usan, ¿está bien tener 2 escenarios exitosos si el dado o el entonces es distinto? RTA: si, además dependiendo el sistema puedo tener 2 escenarios fallidos, 1 por usuario incorrecto y otro por clave, o un solo escenario general donde no se controla que es lo incorrecto del inicio de sesión (es más expresivo hacer 2 escenarios).

#### Practica 3 Casos de uso:
-Pregunta genérica: ¿Las precondiciones son cuando el sistema puede de antemano verificarlo? RTA: si. Se puede pensar como que cuando las precondiciones no se cumplen entonces el botón de la interfaz que permite ejecutar ese CU está deshabilitado. Las cosas que se verifican en el mismo cu no pueden ser precondiciones.

-Se pueden tener 2 pasos alternativos al mismo paso? RTA: SE PUEDE PERO EVITAR, generalmente si tenes que tener 2 pasos alternativos al mismo paso algo estas haciendo raro.

-Se puede en un paso alternativo volver a un paso que todavía no pasó? RTA: SI, en el paso alternativo 4 se puede retornar al paso 7.

-Generalmente, los pasos alternos casi siempre son del sistema, exceptuando los casos en donde el actor tiene que aceptar/rechazar algo, en ese caso se puede tener en curso normal que el actor acepta y en caso alterno que el actor rechaza y fin de cu, pero si no, casi siempre los cursos alternos son del sistema.

-Generalmente, cuando un caso alternativo te lleva a los primeros pasos, casi siempre es lo mismo retornar que finalizar el CU.

-Se usan depends? no hice ninguno RTA: porque no hay en la práctica, en la práctica se representan los depends con precondiciones.

-Pregunta genérica: ¿es necesario poner todos los campos que el usuario tiene que ingresar? RTA: Es necesario ponerlo del lado del sistema pero no del lado del usuario, con poner "El usuario ingresa los datos correspondientes" bastaría.

-Cuando por ejemplo tengo que mostrar una lista y esa lista por x motivo puede quedar vacía, contemplar poner un paso alterno que informe que no hay nada que poner en la lista por x razón.

-Cuando un cu es USES de otros 2 o más cus en precondiciones va "Se debe haber ejecutado el CU “cu1” o “cu2”." más que nada para "justificar" que el primer paso lo da el sistema.

-La flecha de herencia apunta de un actor a DE QUIEN hereda, osea podríamos decir actor 2 hereda de (flechita a) actor 1, actor 2 ES UN actor 1.

#### Practica 4 Diagramas de Transición de Estados:
-PUEDE haber eventos sin acciones, pero no son tan comunes, generalmente en un evento el sistema hace algo pero no es obligatorio.

-si ocurre un evento que no esta modelado, el estado sigue funcionando en el mismo estado porque ese evento no se modelo ninguna transición para ese evento.

-todos los estados deben tener salida.

-todos los estados deben tener al menos una entrada.

-debe haber 1 y solo 1 estado inicial.

-la transición de inicio no tiene que tener condiciones porque no tiene sentido.

-los estados iniciales y finales no tienen nombre como el resto de estados.

-las acciones (siempre acciones del sistema) se pueden escribir de 2 maneras: "Se enciende el motor" o "Encender el motor" (encender verbo en infinitivo) ambas están bien, algunos profes prefieren el verbo en infinitivo y generalmente quedan acciones mas cortas de escribir.

-puedo tener 2 o mas transiciones iguales? RTA: no, puede ser identico el evento que genere la transición pero deben diferir las condiciones para que sea deterministico el modelo osea, que al suceder un evento suceda 1 y solo 1 transición. En el caso en el que tengo 2 transiciones de evento y acciones idénticas (ósea solo difieren en la condición) esas transiciones deberían apuntar a estados distintos o una de esas transiciones no va. 

-como identificar un estado? RTA: los estados merecen existir cuando se espera una interacción de un usuario, o por cuestiones internas del sistemas por ej: cuando el sistema tiene algo que puede interrumpir el funcionamiento como un timer o un sensor de temperatura que detiene la maquina a tal temperatura. GENERALMENTE: "esperando x cosa".

-cuando salgo de un estado para ir a otro, generalmente debería deshabilitar botones que ya no se van a usar y habilitar los nuevos que va a tener el nuevo estado, esto depende de quien lo corrija porque algunos profs no lo ven "tan necesario" pero mientras mas cosas aclares que habilitas y deshabilitas, mas claro queda el diagrama (en los ejercicios con displays son donde mas hay que habilitar y deshabilitar botones).

#### Practica 5 Redes de Petri:

-¿Una transición puede tener dos acciones en el nombre? RTA: Si se puede, por ejemplo, "Terminar de firmar y se retira".

-Es conveniente que las transiciones finales solo reciban un arco.

-No es lo mismo despachar un GRUPO de 4 cajas que despachar por ejemplo UN PAQUETE con 4 cajas adentro, porque un grupo de 4 cajas es igual a 4 cajas juntas (4 tokens), UN paquete (un token) que tiene adentro 4 cajas no es lo mismo que 4 cajas juntas y nada mas.


<p align="center">
    <img src= "https://i.postimg.cc/RFj3cHcM/1.jpg" alt = "img1"/>
</p>