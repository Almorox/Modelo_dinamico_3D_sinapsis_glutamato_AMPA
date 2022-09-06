# Modelo_dinamico_3D_sinapsis_glutamato_AMPA

El archivo ejecutable de CellBlender, *Sinapsis_glutamato_AMPA.blend*, simula 5 ms de una sinápsis química en la que el axón (elemento presináptico) libera una vesícula con 5000 moléculas de glutamato (neurotransmisor) a la hendidura sináptica para que este interaccione con los receptores AMPA localizados en la cabeza dendrítica (elemento postsináptico).

Al principio de la simulación, todos los receptores se encuentran en la conformación C0, sin embargo, según 
transcurre el tiempo, se empiezan a observar distintas conformaciones. Este cambio de conformación se debe a 
reacciones bien estudiadas (*Franks et al., 2002*) que se definen en el modelo con constantes catalíticas que toman 
valores concretos. Algunas de estas reacciones implican la participación del glutamato y otras no. Cada conformación 
se puede diferenciar visualmente por su color particular.

El sistema está configurado de forma que las moléculas de glutamato no pueden pasar dentro del axón ni de la 
dendrita, por lo que difunden (con una constante de difusión también definida por el usuario) a lo largo de la 
hendidura sináptica hacia el exterior, chocando en algún momento con las paredes de un volumen (objeto “Recinto”) que 
engloba a los elementos sinápticos y que representa las membranas de las células del entorno. Cuando el glutamato 
choca contra este recinto, desaparece.

En este archivo se ha definido un step time de conteo de variables de 1e−5
segundos, de modo que las variables son  contadas 500 veces hasta que se acabe el tiempo de simulación de 5 ms. Las variables que se cuentan por defecto son: 

* El número de moléculas de glutamato en la hendidura sináptica.
* El número de moléculas de glutamato en todo el recinto.
* El número de receptores AMPA en la conformación O. 

El modelo devuelve estos conteos en archivos que, posteriormente, pueden ser tratados y estudiados gráficamente como se muestra en el archivo *objetos_parametros_resultados.pdf*. En él se ofrece una descripción más detallada de la configuración del sistema y el tipo de información que devuelve.

Bibliografía.
Kevin M. Franks, Thomas M. Bartol, Jr, and Terrence J. Sejnowski. 2002. Franks, K. M., Bartol, T. M., & Sejnowski, 
T. J. (2002). A Monte Carlo model reveals independent signaling at central glutamatergic synapses. Biophysical 
journal, 83(5), 2333-2348
