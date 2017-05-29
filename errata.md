# ESTheR - Fe de Erratas

* Si bien el enunciado no especifica el archivo de configuración del Proceso CPU, es necesario que contenga al menos, los datos de conexión con el Kernel y con la Memoria.

* El enunciado no especifica como se tiene que desarrollar la cache en el proceso Memoria, detallando que cada entrada debe contener un identificador del proceso, un nro de pagina y un contenido de la pagina. Dadas las múltiples interpretaciones de como manejar el contenido de cada pagina en las entradas, se llegó a la conclusion que puede ser desarrollado como el grupo lo considere correcto, siempre y cuando justifiquen su decision en la evaluacion final.

* Según propuesto por el Enunciado, la Memoria no va a poder asignar paginas a un proceso en la cache cuando esta este llena. Esto no es asi ya que la asignacion de paginas es **global**, por lo tanto, aunque la cache este llena *siempre se le va a poder asignar una pagina* a la misma siguiendo el algoritmo de remplazo de paginas.

* El estado NEW, en la planificación del Kernel, tendrá su representación como una cola, manteniendo los procesos en ella hasta que el grado de multiprogramación permita su paso a READY. Ante una disminución del grado de multiprogramación, se debe dejar finalizar los procesos ANSISOP hasta obtener el nuevo grado.

* La unica razon por la cual un proceso se puede bloquear en este TP es debido a los semaforos. Las syscalls sobre el FS como tambien sobre la gestion del heap y variables globales no bloquean el proceso ansisop

* Según propuesto por el Enunciado, la interfaz de Memoria no puede liberar páginas de un proceso. 
```
Liberar Página de un Proceso
  Parámetros: [Identificador del Programa] [Número de Página elegida]
  Ante un pedido de liberación de página por parte del kernel, el proceso memoria deberá liberar
  la página que corresponde con el número solicitado. En caso de que dicha página no exista
  o no pueda ser liberada, se deberá informar de la imposibilidad de realizar dicha operación
  como una excepcin de memoria.
```
