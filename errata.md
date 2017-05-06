# ESTheR - Fe de Erratas

* El enunciado no especifica el archivo de configuración del Proceso CPU, pero necesita uno que contenga, al menos, los datos de conexión con el Kernel, y posiblemente también con la Memoria.

* El enunciado no especifica como se tiene que desarrollar la cache en el proceso Memoria, dice que cada entrada debe contener un identificador del proceso, un nro de pagina y un contenido de la pagina; de aca surgen muchas interpretaciones de como manejar el contenido de cada pagina en las entradas, luego de muchas interpretaciones y dicusiones se llego a la conclusion que puede ser desarrollado como lo deseen siempre y cuando justifiquen su decision en la evaluacion final.

* El enunciado dice que la Memoria no va a poder asignar paginas a un proceso en la cache cuando esta este llena, esto no es asi ya que la asignacion de paginas es global, por lo tanto, aunque la cache este llena siempre se le va a poder asignar una pagina a la misma siguiendo el algoritmo de remplazo de paginas.

* El estado NEW ,en la planificacion del Kernel, tiene una cola, y no cuenta para el grado de multiprogramación.
